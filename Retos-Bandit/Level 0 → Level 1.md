## Objetivo
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Datos de acceso al nivel

## Solución
```Shell
bandit0@bandit:~$ whoami
bandit0

bandit0@bandit:~$ pwd
/home/bandit0

bandit0@bandit:~$ ls
readme

bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
## Notas adicionales
|Comando|Descripción|
|-----------|----------|
|cat |Nos ayuda a ver el contenido de un archivo ASCII|

## Referencias