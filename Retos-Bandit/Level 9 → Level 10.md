## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de acceso al nivel
Password: EN632PlfYiZbn3PhVK3XOGSlNInNE00t
## Solución

``` shell
bandit9@bandit:~$ cat data.txt | strings -n 12 | grep ==
4========== the#
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
## Notas adicionales

|Comando|Descripción|Ejemplo|
|-----------|-------------|--------|
|strings |despliega las cadenas que son imprimibles |cat data.txt l strings|
|strings -n|Podemos identificar el tamaño de la cadena|strings -n 12|
## Referencias