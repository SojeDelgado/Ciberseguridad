## Objetivo
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/5/fixme2.py)
## Solución

Como dice el error, faltó un = a la sentencia if para arreglar el problema
```bash
sojedelgado-picoctf@webshell:~$ python fixme2.py 
  File "/home/sojedelgado-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
sojedelgado-picoctf@webshell:~$ nano fixme2.py 
sojedelgado-picoctf@webshell:~$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
```

## Notas adicionales

## Referencias