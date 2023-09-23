## Objetivo

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think
## Datos de acceso al nivel
ssh bandit20@bandit.labs.overthewire.org -p 2220
Password: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
## Solución

```bash
bandit20@bandit:~$ bandit20@bandit:~$ ./suconnect 5050
Could not connect
bandit20@bandit:~$ nc -lnvp 5050 <<< "VxCazJaVykI6W36BkBU0mJTCM8rR95XT" &
[1] 2322846
bandit20@bandit:~$ Listening on 0.0.0.0 5050

bandit20@bandit:~$ ./suconnect 5050
Connection received on 127.0.0.1 41920
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
```

## Notas adicionales

## Referencias
