## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## Datos de acceso al nivel
``` cmd
ssh bandit2@bandit.labs.overthewire.org -p 2220
```
## Solución

``` bash
bandit2@bandit:~$ pwd
/home/bandit2

bandit2@bandit:~$ ls
spaces in this filename

bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory

bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
## Notas adicionales
Cuando un archivo contiene espacios en flanco, tendremos que colocarlo entre comillas "".

## Referencias