#### Description

How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/238/atbash.jpg).

#### Solución
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ steghide -- extract -sf atbash.jpg
steghide: unknown command "--".
steghide: type "steghide --help" for help.
                                                                                                
┌──(kali㉿kali)-[~/Downloads]
└─$ steghide --extract -sf atbash.jpg 
Enter passphrase: 
wrote extracted data to "encrypted.txt".
                                                                                                
┌──(kali㉿kali)-[~/Downloads]
└─$ cat encrypted.txt                
krxlXGU{zgyzhs_xizxp_8z0uvwwx}
```

Nos da una cadena de texto encriptada.
Al abrir la imagen dice: Atbash cifer
Siendo este el cifrado de la cadena de texto y al descifrarlo nos da:
picoCTF{atbash_crack_8a0feddc}