## Objetivo
After all this `git` stuff its time for another escape. Good luck!## Objetivo
## Datos de acceso al nivel
ssh bandit32@bandit.labs.overthewire.org -p 2220
**_Password:_** rmCBvG56y58BXzv98yZGdO7ATVL5dW8y

## Solución

Cada comando insertado nos lo convierte a mayúsculas.
Como se trata de un shell interactivo, tenemos la posibilidad de ejecutarlo nuevamente.
Si usamos la variable $0.
```bash
WELCOME TO THE UPPERCASE SHELL
>> clear
sh: 1: CLEAR: Permission denied
>> ls
sh: 1: LS: Permission denied
>> LS
sh: 1: LS: Permission denied
>> $0
$ pwd
/home/bandit32
$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Apr 23 18:04 .
drwxr-xr-x 70 root     root      4096 Apr 23 18:05 ..
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
-rwsr-x---  1 bandit33 bandit32 15128 Apr 23 18:04 uppershell
$ cat /etc/bandit_pass/bandit33
odHo63fHiFqcWWJG9rLiLDtPm45KzUKy
```
## Notas adicionales

## Referencias