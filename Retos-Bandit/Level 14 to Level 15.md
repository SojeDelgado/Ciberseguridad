# Level 14

## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos de acceso al nivel
ssh bandit14@bandit.labs.overthewire.org -p 2220
Password: fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
## Solución

``` shell
bandit14@bandit: nc -v localhost 30000
Connection to localhost (127.0.0.1) 30000 port [tcp/*] succeeded!
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```

## Notas adicionales

|Comando|Descripción|
|-----------|---------|
|nc |Sirve para conectarse a un puerto|

## Referencias