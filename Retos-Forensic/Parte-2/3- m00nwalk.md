## Objetivo
Decode this [message](https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav) from the moon.
## Solución

Instalar el siguiente repositorio en kali https://github.com/colaclanth/sstv.git y seguir las instrucciones de instalación.
Después colocar en la terminal
```bash
kali㉿kali)-[~/Downloads]
└─$ sstv -d message.wav -o img.jpg
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [##############################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
                                                                                
┌──(kali㉿kali)-[~/Downloads]
└─$ open img.jpg
```

Y al darle open img modificamos la orientación de la imagen y nos aparecerá lo siguiente:
![[Screenshot_1 1.png]]
## Notas adicionales

## Referencias