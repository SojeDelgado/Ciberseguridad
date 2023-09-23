## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de acceso al nivel
Password: TESKZC0XvTetK0S9xNwm25STk5iWrBvP

## Solución
``` shell
bandit8@bandit:~$ whoami
bandit8

bandit8@bandit:~$ pwd
/home/bandit8

bandit8@bandit:~$ ls -la
total 56
drwxr-xr-x  2 root    root     4096 Apr 23 18:04 .
drwxr-xr-x 70 root    root     4096 Apr 23 18:05 ..
-rw-r--r--  1 root    root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root    root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit9 bandit8 33033 Apr 23 18:04 data.txt
-rw-r--r--  1 root    root      807 Jan  6  2022 .profile

bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
## Notas adicionales

|Comando|Descripción|Ejemplo|
|-----------|-------------|-----------|
|sort |Ordena lineas de texto| cat data.txt l sort|
|uniq -c |Nos muestra la cantidad de lineas repetidas|
|uniq -u |Nos muestra la linea diferente|

## Referencias