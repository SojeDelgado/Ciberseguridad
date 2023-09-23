## Objetivo
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.
## Datos de acceso al nivel
ssh bandit25@bandit.labs.overthewire.org -p 2220
Password: p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
## Solución

```bash
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p 2220
```
Hacemos chica la pantalla para que no cargue por completo, al momento de estar cargando la pantalla tecleamos v y escribirmos /etc/bandot_pass/bandit36

c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
## Notas adicionales
more Muestra el porcentaje que cabe en pantalla

## Referencias