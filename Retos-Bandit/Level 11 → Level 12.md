# Level 11

## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos de acceso al nivel
bandit11@bandit.labs.overthewire.org -p 2220
Password: 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
## Solución
```bash
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
``` 

O simplemente podemos ir a una página en internet que nos ayude a decodificar RO13

## Notas adicionales

|Comando|Descripción|
|-----------|---------|
|tr |Nos ayuda a decodificar en formato ROT 13|

## Referencias
https://en.wikipedia.org/wiki/ROT13