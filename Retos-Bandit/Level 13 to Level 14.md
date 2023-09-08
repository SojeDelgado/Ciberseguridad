# Level 13

## Objetivo
The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on
## Datos de acceso al nivel
Password: wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
ssh bandit13@bandit.labs.overthewire.org -p 2220

## Solución
Utilizamos una llave privada que nos dio bandit13. 
ssh -i sshkey.private bandit14 @localhost -p 2220
Y entramos a bandit14
Y ahora podremos ver la contraseña sin problema
``` bash
cat /etc/bandit_pass/bandit14
bandit14@bandit: cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```

## Notas adicionales

## Referencias