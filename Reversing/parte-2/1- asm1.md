#### Description

What does asm1(0x2e0) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/f1c2358ff7d1e9386e41552c549cf2f6/test.S)

#### Solución

1. Abrir con cat el archivo
2. Siguiendo las instrucciones de la pila. Nos dice:

	<+3>:   cmp    DWORD PTR [ebp+0x8],0x3fb 
	ebp+0x8 = 0x2e0
	Si 0x2e0 > 0x3fb False

Entonces continuamos a la siguiente línea:
	<+12>:  cmp    DWORD PTR [ebp+0x8],0x280
	0x2e0 != 0x280 True
Entonces nos iremos a la línea que nos indica que es la 29:
	jne    0x50a <asm1+29>
	<+29>:  mov    eax,DWORD PTR [ebp+0x8]
	<+32>:  sub    eax,0xa

Nos dice que veamos la comparación de:
hex(0x2e0-0xa) = 0x2d6
El resultado se almacena en la pila
registers
[ 0x2d6 ] eax

Pasamos a la siguiente instrucción
<+35>:  jmp    0x529 <asm1+60>

<+60>:  pop    ebp
Suelta lo que hay dentro de la pila
La bandera es lo que hay dentro: 0x2d6


