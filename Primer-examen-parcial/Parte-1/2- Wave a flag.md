## Objetivo
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm) has extraordinarily helpful information...
## Solución

```bash
ojedelgado-picoctf@webshell:~$ ls
README.txt  warm
sojedelgado-picoctf@webshell:~$ chmod +x warm
sojedelgado-picoctf@webshell:~$ ./warm -h     
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}
```
## Notas adicionales
|Comando|Descripción|
|---|---|
|wget| Descargar un archivo desde la terminal |
|chmod| nos permite cambiar los permisos de un archivo|

## Referencias
