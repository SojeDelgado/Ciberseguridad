# Level 10

## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

## Datos de acceso al nivel
bandit10@bandit.labs.overthewire.org -p 2220
Password: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
## Solución

```bash
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
## Notas adicionales

|Comando|Descripción|
|-----------|---------|
|base64 -d |Decodifica en formato base64|
## Referencias