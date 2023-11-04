## Objetivo
This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag).
## Solución

```bash
sojedelgado-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag
--2023-09-25 16:50:37--  https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                              100%[==========================================================>]      34  --.-KB/s    in 0s      

2023-09-25 16:50:37 (15.8 MB/s) - 'flag' saved [34/34]

sojedelgado-picoctf@webshell:~$ ls
README.txt  flag
sojedelgado-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_4a2b35fd}
```
## Notas adicionales

wget nos ayuda a descargar archivos desde terminal
## Referencias
