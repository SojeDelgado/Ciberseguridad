### Descripción
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/4c996ecfb7fbada15a9799511f24dc99/shark1.pcapng).
### Solución
Al descargar la imagen lo abrimos con Wireshark
Le damos al follow/TCP stream
En el paquete 5 encontramos un pedazo de bandera
Esta encriptada con Rot13
y nos da la bandera:

picoCTF{p33kab00_1_s33_u_deadbeef}