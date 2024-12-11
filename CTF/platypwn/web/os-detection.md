

> [!Description] ## OS Detection
> A new service has been deployed that uses advanced algorithms to detect your Operating System. What an invasion of privacy! Can you pwn it?

**Web:**


![[ctf_platypwn_os-detection.png]]

We can see that this website jst get the `User-Agent` header from the request and displays it directly 

*Source code:*

![[ctf_platypwn_os-detection_2.png]]

this seems to render the template directly from the file let's try if it's vulnerable to SSTI

![[ctf_platypwn_os-detection_3.png]]

Yes!! It indeed worked perfectly







