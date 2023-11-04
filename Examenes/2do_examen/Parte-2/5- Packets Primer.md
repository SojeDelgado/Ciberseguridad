### Descripción
Download the packet capture file and use packet analysis software to find the flag.

- [Download packet capture](https://artifacts.picoctf.net/c/196/network-dump.flag.pcap)
### Solución
```bash
sojedelgado-picoctf@webshell:~$ ls
README.txt  network-dump.flag.pcap
sojedelgado-picoctf@webshell:~$ cat network-dump.flag.pcap 
òk&NarJ''E<P@@

n#('ԶA
dk&NaJ''E<@@"

#(n&'Է*O
hÍdk&Na`B''E4P@@

n#('Է&9
ehk&Na;~''EpP@@ѳ

n#('Է&u
ehp i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ 0 1 b 0 a 0 d 6 }
k&NaaB''E4g@@

#(n&'Ui
hčep&Na(
        <'ss

p&NaX
     *'99
's
p&Na28*'99

p&Na;<'ss
'9
sojedelgado-picoctf@webshell:~
```
picoCTF{p4ck37_5h4rk_01b0a0d6}