## Objetivo
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
ssh bandit29@bandit.labs.overthewire.org -p 2220
**Password:** tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
## Solución

Al querer acceder a los commit, está encriptada la contraseña.
Verificamos las ramas existentes.
Cambiamos a la rama dev.
Y volvemos a revisar los commits.
```bash
bandit29@bandit:/tmp/soje2/repo$ git log -p
commit 4bd5389f9f2b9e96ba517aa751ee58d051905761 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    fix username

diff --git a/README.md b/README.md
index 2da2f39..1af21d3 100644
--- a/README.md
+++ b/README.md
@@ -3,6 +3,6 @@ Some notes for bandit30 of bandit.

 ## credentials

-- username: bandit29
+- username: bandit30
 - password: <no passwords in production!>


commit 1a57cf10158f133c4f40ff82251f605a7618631d
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    initial commit of README.md

diff --git a/README.md b/README.md
new file mode 100644
index 0000000..2da2f39
--- /dev/null

bandit29@bandit:/tmp/soje2/repo$ git branch -r
  origin/HEAD -> origin/master
  origin/dev
  origin/master
  origin/sploits-dev
bandit29@bandit:/tmp/soje2/repo$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'

bandit29@bandit:/tmp/soje2/repo$ git log -p -1
commit 13e735685c73e5e396252074f2dca2e415fbcc98 (HEAD -> dev, origin/dev)
Author: Morla Porla <morla@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    add data needed for development

diff --git a/README.md b/README.md
index 1af21d3..a4b1cf1 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for bandit30 of bandit.
 ## credentials

 - username: bandit30
-- password: <no passwords in production!>
+- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
```

## Notas adicionales
|Comando| Descripción|
|---|---|
|git branch -r|Muestra las distintas ramas del repositorio|
|git checkout _nombreDeLaRama_|Cambia a la rama indicada|
## Referencias