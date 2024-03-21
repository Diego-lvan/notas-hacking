## Objetivo
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
## Solución

picoCTF{c0rrupt10n_1847995}


Al hacer file mystery nos regresa data, esto significa que no es capaz de indentificar el tipo de archivo.
Pero podemos  hacer xxd al archivo y ver que es un PNG
Abrimos hexeditor y cambiamos los 8 primeros bytes por los que nos indica la documetación x89\x50\x4E\x47\x0D\x0A\x1A\x0A.

Ahora si le hacemos file mystery.png el sistema si lo identifica como png, pero si hacemos pngcheck sigue habiendo errores.

Los errores que nos marca es en los chunk pHYs por lo que tenemos que corregir ese chunk


## Notas adicionales
pngcheck checa que un archivo png no este dañado

## Referencias
https://en.wikipedia.org/wiki/PNG
