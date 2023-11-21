#### Description

This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program. You can download the file from [here](https://artifacts.picoctf.net/c/508/asciiftw).

### Solución
Al abrir el archivo con Ghidra podemos ver que en el apartado main dice que la bandera empieza con 0x70:
![[Screenshot_3.png]]
Al darle click podemos apreciar de mejor manera los hexadecimales:
![[Screenshot_1.png]]
Copiamos los hexadecimales:
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x41 0x53 0x43 0x49 0x49 0x5f 0x49 0x53 0x5f 0x45 0x41 0x53 0x59 0x5f 0x38 0x39 0x36 0x30 0x46 0x30 0x41 0x46 0x7d

Y al pasarlos a char nos da:
picoCTF{ASCII_IS_EASY_8960F0AF}
