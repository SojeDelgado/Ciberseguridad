## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
## Solución

Al entrar al código de python, el programa contenía la contraseña de este modo:
chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36). Siendo los caracteres: "de76".

```bash
sojedelgado-picoctf@webshell:~$ ls
README.txt  level2.flag.txt.enc  level2.py
sojedelgado-picoctf@webshell:~$ nano level2.py 
sojedelgado-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
```

## Notas adicionales

## Referencias