# Level 0
	http://overthewire.org/wargames
## Objetivo
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port 2220. The username is **bandit0** and the password is **bandit0**. Once logged in, go to the [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) page to find out how to beat Level 1.
## Datos de acceso al nivel
	user: bandit0@bandit.labs.overthewire.org 
	servidor: 2220
	password: bandit0

## Solución
```bash 
ssh bandit0@bandit.labs.overthewire.org -p 2220 
```

## Notas adicionales

|**Comando**|**Descripción**|
|----------|-------------|
|pwd |Me indica el directorio actual|
|whoami|Saber el usuario actual|
|cd /|Me lleva al directorio raíz|
|exit|Cerrar sesión|

|**Atajo**|**Descripción**|
|------|-------------|
|ctrl + a|Ir al inicio de la línea|
|ctrl + b|Ir al final de la línea|


Generar llaves SSH
``` cmd
C:\Users\user>ssh-keygen
```
## Referencias