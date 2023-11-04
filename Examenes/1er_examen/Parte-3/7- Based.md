## Objetivo
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 15130`.

## Solución

01101111 01110110 01100101 01101110
Son numero binarios:
01101111 -> 111 (ASCII: 'o') 
01110110 -> 118 (ASCII: 'v') 
01100101 -> 101 (ASCII: 'e') 
01101110 -> 110 (ASCII: 'n')

163 164 162 145 145 164 
representan valores numéricos de caracteres en código ASCII:
163 -> 's' 
164 -> 't' 
162 -> 'r' 
145 -> 'e' 
145 -> 'e' 
164 -> 't'

737472656574
Tambien en código ASCII
737 -> 's'
472 -> 't'
656 -> 'r'
574 -> 'e'
574 -> 'e'
656 -> 't'

```bash
sojedelgado-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 15130
Let us see how data is stored
oven
Please give the 01101111 01110110 01100101 01101110 as a word.
...
you have 45 seconds.....

Input:
oven
Please give me the  163 164 162 145 145 164 as a word.
Input:
street
Please give me the 737472656574 as a word.
Input:
street
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_02167de8}
```

## Notas adicionales

## Referencias