## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.
## Solución

Al ver el código de Python pude ver cual era el password para que me entregara la bandera.

```bash
sojedelgado-picoctf@webshell:~$ nano level1.py 
sojedelgado-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
'picoCTF{545h_r1ng1ng_fa343060}'
```

## Notas adicionales

## Referencias