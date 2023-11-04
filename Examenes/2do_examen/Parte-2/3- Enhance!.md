### Descripción
Download this image file and find the flag.

- [Download image file](https://artifacts.picoctf.net/c/101/drawing.flag.svg)
### Solución

Al darle cat al archivo nos arroja un HTML.
Buscamos pico. Nada.
Pero al revisar el archivo nos damos cuenta que en las etiquetas tspan se encuentran pedazos de bandera
``` bash
sojedelgado-picoctf@webshell:~$ cat drawing.flag.svg | grep pico
sojedelgado-picoctf@webshell:~$ cat drawing.flag.svg | grep tspan
       id="text3723"><tspan
         id="tspan3748">p </tspan><tspan
         id="tspan3754">i </tspan><tspan
         id="tspan3756">c </tspan><tspan
         id="tspan3758">o </tspan><tspan
         id="tspan3760">C </tspan><tspan
         id="tspan3762">T </tspan><tspan
         id="tspan3764">F { 3 n h 4 n </tspan><tspan
         id="tspan3752">c 3 d _ 2 4 3 7 4 6 7 5 }</tspan></text>
```

picoCTF{3nh4nc3d_24374675}