## Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo` via the port `2220`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
ssh bandit30@bandit.labs.overthewire.org -p 2220
**Password:** xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
## Solución
Al intentar verificar los branches y el historial de commits no hay contraseña.

```bash
bandit30@bandit:/tmp/soje3/repo$ git tag
secret
bandit30@bandit:/tmp/soje3/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
```

## Notas adicionales
|Comando|Descripción|
|---|---|
|git tag|Muestra los tags del repositorio|

Tags en git son referencias que apuntan a puntos concretos en el historial de Git.
Generalmente, el etiquetado se usa para capturar un punto en el historial que se utiliza para una publicación de versión marcada (por ejemplo, v1. 0.1). Una etiqueta es como una rama que no cambia.
## Referencias
https://www.atlassian.com/es/git/tutorials/inspecting-a-repository/git-tag#:~:text=Las%20etiquetas%20son%20referencias%20que,una%20rama%20que%20no%20cambia.