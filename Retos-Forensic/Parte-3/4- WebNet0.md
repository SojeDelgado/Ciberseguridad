## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
## Solución
Abrimos con wireshark.
Edicion, preferencias, protocolos y seleccionamos TLS, colocamos la llave.
Volvemos a darle a edit, find packet, lo colocamos tipo string, y colocamos detalles de paquete y buscamos picoCFT y nos dará:
Pico-Flag: picoCTF{nongshim.shrimp.crackers}
## Notas adicionales

## Referencias