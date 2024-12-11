


> [!Description] ## Pretty HTML Page
> 
> I made a pretty HTML page. It can even give you a flag if you write “flag”! But for security reasons, as soon as you write “flag”, your input will get redacted. Sorry for that :)


**Web interface:**

![[ctf_platypwn_pretty-html-page_1.png]]

**Source code**

```php
<?php

if ($_SERVER["REQUEST_METHOD"] == "POST") {
	$input = $_POST["input_string"];

	if (mb_strpos($input, "flag") !== false) {
		$a = mb_strpos($input, "flag");
		echo "<p>Input contains 'flag' at position " . $a . "</p>";
		$b = mb_substr($input, 0, $a);
		$input = $b . "REDACTED";
		 echo "<p>You wrote: " . htmlentities($input, ENT_QUOTES, 'UTF-8') . "</p>";

	}

	else {
		echo "<p>Input does not contain 'flag'</p>";
		$b = $input;
		echo "<p>You wrote: " . htmlentities($b, ENT_QUOTES, 'UTF-8') . "</p>";
	}
	
	if (mb_strpos($b, "flag") !== false) {

		$file_to_flag = "/flag/flag.txt";

		$flag = file_get_contents($file_to_flag);

		echo "<p>Congrats! Here is your flag: " . $flag . "</p>";
	}

}

?>
```


After googling some PHP tricks, I discovered a bug due to the inconsistent interaction between `mb_strpos`and `mb_substr`. Specifically, when `mb_strstr`it encounters a leading byte of UTF-8, it will skip 3 subsequent bytes. This means that for `mb_substr`, the first four bytes of a UTF-8 character will be considered one character, and the next character will be processed from the next index.

![[ctf_platypwn_pretty-html-page_2.png]]


But in our case the function must skip the string `flag (4bytes)` we do it by placing another UTF-8 character at index 1 (4th byte)




so the payload looks like 
```
%F0%41%41%41flag
```


 how it works:
`mb_strpos("\xF0\x41\x41\x41\xF0flag", "flag")`  ---> `4`

As this function returns 4 as the index of the string we must place the string from indices `0 to 3` 

![[ctf_platypwn_pretty-html-page_3.png]]

Using burp to intercept the request and change the payload

![[ctf_platypwn_pretty-html-page_4.png]]

`PP{c0Unt1n6_ch42AC73r5-15_h4rD::9BKDbLvEy3RV}`


References:
https://www.sonarsource.com/blog/joomla-multiple-xss-vulnerabilities/

[https://hackmd.io/@CaRZODiyRTmwgiK0D4Rf8A/B1rSJYl70?utm_source=preview-mode&utm_medium=rec](https://hackmd-io.translate.goog/@CaRZODiyRTmwgiK0D4Rf8A/B1rSJYl70?utm_source=preview-mode&utm_medium=rec&_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=en-US&_x_tr_pto=wapp#Bypass-_santize_secret-via-werid-interacting-mb_strpos-and-mb_substr)

https://github.com/php/php-src/pull/12913
