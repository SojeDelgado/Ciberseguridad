## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## Datos de acceso al nivel
ssh bandit16@bandit.labs.overthewire.org -p 2220
Password: JQttfApK4SeyHwDlI9SXGR50qclOAil1
## Solución

```bash

bandit16@bandit:~$ nmap localhost -p 31000-32000
Starting Nmap 7.80 ( https://nmap.org ) at 2023-09-13 16:34 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00013s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.10 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31790

bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
```

## Notas adicionales

|Comando|Descripción|
|---|---|
|nmap localhost| Me dice los puertos que están abiertos <br> (Escanea los primeros 1000)|
|nmap localhost -p 31000-32000|Indica el rango de puertos a analizar|


## Referencias