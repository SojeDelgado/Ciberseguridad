## Objetivo
There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo` via the port `2220`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel
ssh bandit27@bandit.labs.overthewire.org -p 2220
Password: YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
## Solución

```bash
bandit27@bandit:~$ mktemp -d
/tmp/tmp.iNjaPPWKrj
bandit27@bandit:~$ cd /tmp/tmp.iNjaPPWKrj
bandit27@bandit:/tmp/tmp.iNjaPPWKrj$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...

bandit27@bandit:/tmp/tmp.iNjaPPWKrj$ cd repo/
bandit27@bandit:/tmp/tmp.iNjaPPWKrj/repo$ ls
README
bandit27@bandit:/tmp/tmp.iNjaPPWKrj/repo$ cat README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR
```
## Notas adicionales
Si no se especifica el puerto no tengo acceso al repositorio.
Entonces colocamos localhost:2220

## Referencias
