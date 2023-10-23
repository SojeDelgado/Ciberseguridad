## Objetivo
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/c00c449c3b08daaccacca6f9d5c55d49/Forensics%20is%20fun.pptm)
## Solución

```bash
┌──(kali㉿kali)-[~/Downloads/macro]
└─$ cd ppt/slideMasters/      
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Downloads/macro/ppt/slideMasters]
└─$ ls   
hidden  _rels  slideMaster1.xml
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Downloads/macro/ppt/slideMasters]
└─$ file hidden       
hidden: ASCII text, with no line terminators
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Downloads/macro/ppt/slideMasters]
└─$ cat hidden          
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q
```
desencriptamos en base64 el archivo hidden
Y nos da la bandera:
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}
## Notas adicionales

## Referencias