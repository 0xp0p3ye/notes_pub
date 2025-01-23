

- Full Name: Shanjaikumaar S
- Discord Alias: 0xp0p3ye
- Platform Alias: 0xp0p3ye
- Phone Number: +91 9597157552


##  BRUTEONE

**CRYPTOGRAPHY - CLASSIC CIPHERS** 


**output.txt**

```
44bd7ae60f478fae1061e11a7739f4b94d1daf917982d33b6fc8a01a63f89c21
559aead08264d5795d3909718cdd05abd49572e84fe55590eef31a88a08fdffd
6b23c0d5f35d1b11f9b683f0b0a617355deb11277d91ae091d399c655b87940d
86be9a55762d316a3026c2836d044f5fc76e34da10e1b45feee5f18be7edb177
d2e2adf7177b7a8afddbc12d1634cf23ea1a71020f6a1308070a16400fb68fde
4ae81572f06e1b88fd5ced7a1a000945432e83e1551e6f721ee9c00b8cc33260
a25513c7e0f6eaa80a3337ee18081b9e2ed09e00af8531c8f7bb2542764027e7
a9f51566bd6705f7ea6ad54bb9deb449f795582d6529a0e22207b8981233ec58
8de0b3c47f112c59745f717a626932264c422a7563954872e237b223af4ad643
e632b7095b0bf32c260fa4c539e9fd7b852d0de454e9be26f24d0d6f91d069d3
021fb596db81e6d02bf3d2586ee3981fe519f275c0ac9ca76bbcf2ebb4097d96
acac86c0e609ca906f632b0e2dacccb2b77d22b0621f20ebece1a4835b93f6f0
3f79bb7b435b05321651daefd374cdc681dc06faa65e374e38337b88ca046dea
e3b98a4da31a127d4bde6e43033f66ba274cab0eb7eb1c70ec41402bf6273dd8
043a718774c572bd8a25adbeb1bfcd5c0256ae11cecf9f9c3f925d0e52beaf89
d2e2adf7177b7a8afddbc12d1634cf23ea1a71020f6a1308070a16400fb68fde
cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29
65c74c15a686187bb6bbf9958f494fc6b80068034a659a9ad44991b08c58f2d2
d2e2adf7177b7a8afddbc12d1634cf23ea1a71020f6a1308070a16400fb68fde
2e7d2c03a9507ae265ecf5b5356885a53393a2029d241394997265a1a25aefc6
aaa9402664f1a41f40ebbc52c9993eb66aeb366602958fdfaa283b71e64db123
ca978112ca1bbdcafac231b39a23dc4da786eff8147c4e72b9807785afee48bb
454349e422f05297191ead13e21d3db520e5abef52055e4964b82fb213f593a1
ca978112ca1bbdcafac231b39a23dc4da786eff8147c4e72b9807785afee48bb
2e7d2c03a9507ae265ecf5b5356885a53393a2029d241394997265a1a25aefc6
e3b98a4da31a127d4bde6e43033f66ba274cab0eb7eb1c70ec41402bf6273dd8
3f79bb7b435b05321651daefd374cdc681dc06faa65e374e38337b88ca046dea
454349e422f05297191ead13e21d3db520e5abef52055e4964b82fb213f593a1
d2e2adf7177b7a8afddbc12d1634cf23ea1a71020f6a1308070a16400fb68fde
3e23e8160039594a33894f6564e1b1348bbd7a0088d42c4acb73eeaed59c009d
a1fce4363854ff888cff4b8e7875d600c2682390412a8cf79b37d0b11148b0fa
d2e2adf7177b7a8afddbc12d1634cf23ea1a71020f6a1308070a16400fb68fde
2e7d2c03a9507ae265ecf5b5356885a53393a2029d241394997265a1a25aefc6
aaa9402664f1a41f40ebbc52c9993eb66aeb366602958fdfaa283b71e64db123
ca978112ca1bbdcafac231b39a23dc4da786eff8147c4e72b9807785afee48bb
454349e422f05297191ead13e21d3db520e5abef52055e4964b82fb213f593a1
ca978112ca1bbdcafac231b39a23dc4da786eff8147c4e72b9807785afee48bb
2e7d2c03a9507ae265ecf5b5356885a53393a2029d241394997265a1a25aefc6
e3b98a4da31a127d4bde6e43033f66ba274cab0eb7eb1c70ec41402bf6273dd8
3f79bb7b435b05321651daefd374cdc681dc06faa65e374e38337b88ca046dea
454349e422f05297191ead13e21d3db520e5abef52055e4964b82fb213f593a1
```


![[ctf_defhawk_crypto_bruteone_2.png]]


using crackstation to crack the hashes 

![[ctf_defhawk_crypto_bruteone_3.png]] 

![[ctf_defhawk_crypto_bruteone_4.png]]

![[ctf_defhawk_crypto_bruteone_5.png]]


FLAG: HACK_QUEST{lets_go_character_by_character}








## WHOS SHADOW

WEB - SECURITY MISCONFIGURATION

Description: 
find what user '67896ab1c3d94b4e97baf28c' says


after visiting the products, we can see the api response as given below. Grep the given userID and his review text is the flag!!

![[ctf_defhawk_web_whosshadow_1.png]]


Browser view:
![[ctf_defhawk_web_whosshadow_2.png]]



FLAG: HACK_QUEST{Just wow get it all}








## SHADOW INSIGHT


By entering a wrong Email (or) invalid Email format (or)  existing Email in the signup pages it gives the error code with the flag ;)

![[ctf_defhawk_web_shadowsinsight.png]]


 
 FLAG: HACK_QUEST{shadow_email_leak}









## NOT THAT EASY

Extracting the IMG2.jpg (zip archive) and the extracted text file `txt.txt` contains second half of the flag

```
_steganography}

```

and using `steghide` to crack the IMG_CRC.jpg with the password `101hacking` given in comment of the picture

![[ctf_defhawk_steg_notthateasy.png]]

FLAG: HACK_QUEST{Ways_of_doing_steganography}










## DOCKER AND DANGEROUS

**EXPLOITATION  - BINARY EXPLOITATION**

![[ctf_defhawk_bin_docker_1.png]]

ssh to the remote server using the given credentials `specter:password123`


Adding the given IP `13.127.127.107` to known-hosts

![[ctf_defhawk_bin_docker_3.png]]


We can see that the current shell uses a restricted env (rbash shell) 
and most of the commands like `cat, more,head, less, tail` are not available here  
![[ctf_defhawk_bin_docker_4.png]]

Using echo to view file content `echo $(</flags/flags.txt)`

![[ctf_defhawk_bin_docker_5.png]]

FLAG: HACK_QUEST{restricted_shell_escape_successful}















##   PRETTY -PE

**DIGITAL FORENSICS - FILE ANALYSIS**

![[ctf_defhawk_foren_prettype.png]]
I'm not sure about the exact way but using strings and grep to get the flag.... Cause why not!! ;)

FLAG: HACK_QUEST{pew_pe_pe_exe}









## FOLLOW THE TRACES

**DIGITAL FORENSICS - FILE ANALYSIS**

![[ctf_defhawk_foren_followthetraces.png]]

base64 decoding the strings from the given excel sheet
![[ctf_defhawk_foren_followthetraces_2.png]]

![[ctf_defhawk_foren_followthetraces_3.png]]


FLAG: HACK_QUEST{ransomware_on_system}









## NESTED SECRETS

**MISC - TRIVA CHALLENGES**

![[ctf_defhawk_misc_nestedsecrets.png]]










## STRING CIPHER

**REVERSE ENGINEERING - BINARY EXPLOITATION**


Uploading the given dog file to [dogbolt](https://dogbolt.org/)   
![[ctf_defhawk_bin_stringcipher_1.png]]

A script to decode the numeric flag and reverse the XOR transformation, and extracts a hardcoded flag data sequence

```python
def decode_flag(numeric_flag):
    decoded_flag = ""
    i = 0
    while i < len(numeric_flag):
        # Try decoding as 3-digit ASCII if valid, otherwise 2-digit
        if i + 2 < len(numeric_flag) and int(numeric_flag[i:i+3]) <= 126:
            decoded_flag += chr(int(numeric_flag[i:i+3]))
            i += 3
        else:
            decoded_flag += chr(int(numeric_flag[i:i+2]))
            i += 2
    return decoded_flag

def reverse_xor_transformation():
    # Original transformed string from var_70
    transformed = "XYZ[\\]^_`abcdefghijklmn"

    # Reverse the XOR transformation
    original = ""
    for index, char in enumerate(transformed):
        original += chr(ord(char) ^ index)

    return original

def extract_flag():
    # Extracted hardcoded flag-like data from var_d8
    flag_data = "\x37\x32\x00\x36\x35\x00\x36\x37\x00\x37\x35\x00\x39\x35\x00\x38\x31\x00\x38\x35\x00\x36\x39\x00\x38\x33\x00\x38\x34\x00\x31\x32\x33\x38\x33\x00\x36\x39\x00\x36\x35\x00\x38\x33\x00\x37\x33\x00\x36\x38\x00\x36\x39\x00\x38\x33\x00\x39\x35\x00\x38\x32\x00\x36\x39\x00\x38\x36\x00\x36\x39\x00\x38\x32\x00\x38\x33\x00\x36\x39\x00\x39\x35\x00\x38\x37\x00\x36\x35\x00\x38\x36\x00\x36\x39\x00\x31\x32\x35\x00\x00\x00"

    # Split and decode the flag-like data (null-separated ASCII values)
    flag_parts = flag_data.split("\x00")
    flag = "".join(flag_parts)

    return flag

if __name__ == "__main__":
    # Decode the numeric flag
    numeric_flag = "72656775958185698384123836965837368698395826986698283699587658669125"
    decoded_flag = decode_flag(numeric_flag)
    print(f"Decoded flag: {decoded_flag}")

    # Perform the XOR reversal
    original_string = reverse_xor_transformation()
    print(f"Original string from XOR transformation: {original_string}")

    # Extract the hardcoded flag-like data
    flag = extract_flag()
    print(f"Extracted flag: {flag}")

```


![[ctf_defhawk_rev_stringcipher_3.png]]


FLAG:   HACK_QUEST{SEASIDES_REVERSE_WAVE}




