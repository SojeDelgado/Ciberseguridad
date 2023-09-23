## Objetivo
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo` via the port `2220`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
ssh bandit28@bandit.labs.overthewire.org -p 2220
Password: AVanL161y9rsbcJIsFHuw35rjaOM19nR
## Solución

Bajamos el repositorio. Revisamos el archivo README pero la contraseña está encriptada.
Verificamos los commits del repositorio con git log.

```bash
bandit28@bandit:/tmp/soje/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/soje/repo$ git log -p -1
commit 899ba88df296331cc01f30d022c006775d467f28 (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Sun Apr 23 18:04:39 2023 +0000

    fix info leak

diff --git a/README.md b/README.md
index b302105..5c6457b 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials

 - username: bandit29
-- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
+- password: xxxxxxxxxx

bandit28@bandit:/tmp/soje/repo$
```

## Notas adicionales
|Comandos|Descripción|
|---|---|
|git log|Muestra los commits del repositorio|
|git log -p|Muestra los diff introducidos en cada commit|
|git log -1|Limita la salida solo a la ultima entrada|
## Referencias
https://victorhckinthefreeworld.com/2022/10/24/como-mostrar-los-commits-en-git-realizados-en-una-fecha-concreta/#:~:text=Con%20el%20comando%20git%20log,lo%20hizo%20y%20m%C3%A1s%20informaci%C3%B3n.