## Objetivo

The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.
## Datos de acceso al nivel
ssh bandit18@bandit.labs.overthewire.org -p 2220
Password: hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

## Solución

```bash
C:\Users\josem\OneDrive\Escritorio>ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/cat readme
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```

## Notas adicionales

Se puede ingresar a carpetas desde antes de entrar al servidor colocando las respectivas instrucciones.
## Referencias