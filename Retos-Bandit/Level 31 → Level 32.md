## Objetivo
There is a git repository at `ssh://bandit31-git@localhost/home/bandit31-git/repo` via the port `2220`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
ssh bandit31@bandit.labs.overthewire.org -p 2220
**_Password:_** OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
## Solución
En el archivo README nos indica que hagamos push al repositorio en el branch master.

```bash
bandit31@bandit:/tmp/soje4/repo$ touch key.txt
bandit31@bandit:/tmp/soje4/repo$ echo "May I come in?" > key.txt
bandit31@bandit:/tmp/soje4/repo$ git add key.txt
The following paths are ignored by one of your .gitignore files:
key.txt
hint: Use -f if you really want to add them.
hint: Turn this message off by running
hint: "git config advice.addIgnoredFile false"
bandit31@bandit:/tmp/soje4/repo$ ls -la
total 24
drwxrwxr-x 3 bandit31 bandit31 4096 Sep 23 22:24 .
drwxrwxr-x 3 bandit31 bandit31 4096 Sep 23 22:22 ..
drwxrwxr-x 8 bandit31 bandit31 4096 Sep 23 22:25 .git
-rw-rw-r-- 1 bandit31 bandit31    6 Sep 23 22:22 .gitignore
-rw-rw-r-- 1 bandit31 bandit31   15 Sep 23 22:25 key.txt
-rw-rw-r-- 1 bandit31 bandit31  147 Sep 23 22:22 README.md

bandit31@bandit:/tmp/soje4/repo$ cat .gitignore
*.txt
```

Al parecer el archivo .gitignore especificaba archivos desconocidos intencionalmente para ignorarlos.
Removemos el archivo con rm.
Y volvemos a intentar agregar el archivo al repositorio con add.
```bash
bandit31@bandit:/tmp/soje4/repo$ rm .gitignore
bandit31@bandit:/tmp/soje4/repo$ git add key.txt
bandit31@bandit:/tmp/soje4/repo$ git commit -m "Archivo subido"
[master 159b0de] Archivo subido
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
```

Hacemos un push al repositorio y nos proporciona la clave.
``` bash
bandit31@bandit:/tmp/soje4/repo$ git push origin master
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 326 bytes | 326.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'
```

## Notas adicionales

## Referencias