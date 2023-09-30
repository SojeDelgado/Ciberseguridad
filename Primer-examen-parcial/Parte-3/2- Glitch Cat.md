## Objetivo
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 55826`
## Solución

Al ingresar el comando nos da lo siguiente:
```bash
sojedelgado-picoctf@webshell:~$ nc saturn.picoctf.net 55826
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
```

Para desencriptar la bandera hacemos el siguiente código en python:
```python
# Cadena original
cadena_original = 'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'

# Extraer los valores ASCII en hexadecimal
valores_hex = cadena_original.split('\\x')

# Convertir los valores hexadecimales en caracteres ASCII y concatenarlos
flag_desencriptada = ''
for valor_hex in valores_hex:
    if valor_hex:
        flag_desencriptada += chr(int(valor_hex, 16))

print(flag_desencriptada)

```

## Notas adicionales

## Referencias