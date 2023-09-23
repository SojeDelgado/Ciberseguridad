## Objetivo
The password for the next level is stored in a file called **-** located in the home directory
## Datos de acceso al nivel
``` cmd
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

Password: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
## Solución
``` bash
bandit1@bandit:~$ whoami
bandit1

bandit1@bandit:~$ pwd
/home/bandit1

bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C

bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```

## Notas adicionales
Cuando un archivo comienza con un "-" tenemos que anteponer ./ al nombre o bien especificar la ruta completa de los archivos.
## Referencias
- [Google Search for “dashed filename”](https://www.google.com/search?q=dashed+filename)
- [Advanced Bash-scripting Guide - Chapter 3 - Special Characters](http://tldp.org/LDP/abs/html/special-chars.html)