## Objetivo
Good job getting a shell! Now hurry and grab the password for bandit27!
## Datos de acceso al nivel
ssh bandit26@bandit.labs.overthewire.org -p 2220
Password: c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
## Solución

Mismo que el reto anterior, pero está ves colocamos :shell

set shell=/bin/bash
```bash
bandit26@bandit:~$ ./bandit27-do id
uid=11026(bandit26) gid=11026(bandit26) euid=11027(bandit27) groups=11026(bandit26)
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
```

## Notas adicionales

## Referencias