## Objetivo
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/1b70cffdd2f05427fff97d13c496963f/dolls.jpg)

## Solución
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ binwalk --extract dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378954, uncompressed size: 383938, name: base_images/2_c.jpg
651612        0x9F15C         End of Zip archive, footer length: 22

                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Downloads]
└─$ cd dolls.jpg.extracted
cd: no such file or directory: dolls.jpg.extracted

┌──(kali㉿kali)-[~/Downloads]
└─$ cd _dolls.jpg.extracted

┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ ls
136DA.zip  flag.txt
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ cat flag.txt         
picoCTF{bf6acf878dcbd752f4721e41b1b1b66b}

```
Seguimos extrayendo las imagenes con binwalk hasta encontrar un .txt
Y nos dará la bandera:
picoCTF{bf6acf878dcbd752f4721e41b1b1b66b}