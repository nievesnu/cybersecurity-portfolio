# Data Encoding - TryHackMe

I just completed [Data Encoding](https://tryhackme.com/room/dataencoding?utm_campaign=social_share&utm_medium=social&utm_content=room&utm_source=linkedin&sharerId=687937a5488df707cc460ae1) room on TryHackMe! 

Learning how computer encodes characters, from ASCII to Unicode's UTF.
```
 file.txt with TryHackMe writen in it as ASCII encoded: 01010100 01110010 01111001 01001000 01100001 01100011 01101011 01001101 01100101 00001010
 The file looks like this in hexadecimal: 54 72 79 48 61 63 6b 4d 65 0 and the decimal would be: 124 162 171 110 141 143 153 115 145 012
```

*Finds:* we need an encoding to support other European languages. 
- ASCII uses 7 bits, and with an eighth bit, we get 128 more characters whichare not enough to cover all the letters of the European languages. The ISO/IEC 8859 Series (International Standards) created several standards; each standard covered a set of languages:
ISO-8859-1 (Latin-1): Covered Western European languages like German (ß, ü), French (é, ç), Spanish (ñ, ¿), Italian, Portuguese, Catalan, and Nordic languages (e.g., Icelandic ð/Ð). Check this link(opens in new tab).
ISO-8859-2 (Latin-2): Supported Central/Eastern European languages like Polish (ł, ń), Czech (č, ř), Hungarian (ő, ű), Croatian (đ), Romanian (ș, ț), and Slovak. Check this link(opens in new tab).

It is essential for both the sender and the recipient to use the same encoding; moreover, we need an encoding that can include all the characters from all languages. 
- Unicode: universal character encoding standard. It assigns unique code points to characters from all modern and historical writing systems worldwide.
Unicode supports the interchange, processing, and display of text in diverse languages. In other words, we don’t need to worry about picking a specific encoding standard that is compatible with the language we are using. 

<img width="216" height="175" alt="image" src="https://github.com/user-attachments/assets/0ca7c936-39b1-435b-b709-3806614b8445" />
