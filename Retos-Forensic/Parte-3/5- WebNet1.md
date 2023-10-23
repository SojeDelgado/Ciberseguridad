## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

## Solución
Abrimos con wireShark al igual que el anterior reto, le colocamos la llave.
Le damos a file, export objects as HTTPS, guardamos la única imagen que hay

hacemos un strings con el archivo de la imagen en la terminal y nos dará:


```bash
──(kali㉿kali)-[~/Downloads]
└─$ strings vulture.jpg | grep pico
picoCTF{honey.roasted.peanuts}
```
picoCTF{honey.roasted.peanuts}
## Notas adicionales

## Referencias