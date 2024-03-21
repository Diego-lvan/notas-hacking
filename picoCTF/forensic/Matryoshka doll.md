


## Objetivo
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/5ef2e9103d55972d975437f68175b9ab/dolls.jpg)
## Solución
binwalk extraer de un archivokb
Al hacer binwalk doll.jpg podemos ver que tiene un zip.
Podemos hacer unzip a la imagen un unzip, esto nos genera otra imagen y aplicamos lo mismo hasta que nos de un archivo flag.txt


picoCTF{e3f378fe6c1ea7f6bc5ac2c3d6801c1f}                                                                                                                                                             


## Notas adicionales

## Referencias
