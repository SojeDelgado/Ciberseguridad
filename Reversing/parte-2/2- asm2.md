#### Description

What does asm2(0x4,0x2d) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/ceac75672637589213b952abe32c84b3/test.S)

#### Solución
Mismo que el anterior

+31  0x4 <= 0x5fa1  True

pasamos a linea +20

+20 add 0x2d + 0x1 = 0x2e
+24 add 0x4 + 0xd1 = 0xd5
+31 cmp 0xd5 <= 0x5fa1 True

Todo el tiempo estará dando True.
Pero si dividimos: 0x5fa1 / 0xd1 = 117.13397129186603
Redondeando a 118.

Entonces agarrando el valor en ebp +  0xc 
que es 0x2d su valor a entero es 45

sumamos ese valor al numero de vueltas que tendrá que dar para que el valor sea False en la comparación  = hex(45 + 118) = 0xa3

La bandera es:
__0xa3__
