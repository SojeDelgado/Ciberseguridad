## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.
## Solución

```bash
kali㉿kali)-[~/Downloads]
└─$ cat flag.txt | grep Port | cut -d ' ' -f6 | tr -d ',' | cut -c2- 
000
112
105
099
111
067
084
070
123
112
049
076
076
102
051
114
051
100
095
100
097
116
097
095
118
049
097
095
115
116
051
103
048
125
000
```
Al descifrarlo en cyberchef
picoCTF{p1LLf3r3d_data_v1a_st3g0}
## Notas adicionales

## Referencias