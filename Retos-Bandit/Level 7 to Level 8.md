## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**

## Datos de acceso al nivel
Password: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
## Solución

``` shell
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP

bandit7@bandit:~$ cat data.txt | grep millionth
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
## Notas adicionales

|Comando|Descripción|
|-----------|-------------|
|wc |Permite ver lineas, caracteres y bytes|
|grep |Permite buscar por palabras |
|Ejemplo de grep |"cat data.txt l grep millionth" |


## Referencias