## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## Datos de acceso al nivel

Password: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## Solución
``` shell
bandit6@bandit:~$ whoami
bandit6

bandit6@bandit:~$ bandit6@bandit:~$ find / -size 33c -user bandit7 -group bandit6 2>/dev/null
/var/lib/dpkg/info/bandit7.password

bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```

## Notas adicionales

|Comando|Descripción|
|-----------|---------|
|find / |Busca desde la raíz|
|-user |Permite especificar el usuario|
|-group|Permite especificar por grupo|
|2>/dev/null|Ignora los mensajes con error|

## Referencias
