


## Objetivo
We found this [file](https://mercury.picoctf.net/static/da18eed3d15fd04f7b076bdcecf15b27/tunn3l_v1s10n). Recover the flag.
## Solución

Cambiamos los header de la imagen con hexeditor y cambiamos el tamaño de la imagen y el lugar donde empiezan los datos.


Abrimos la imagen y vemos que aun no se ve la bandera, pero podemos observar que está muy ancha la imagen por lo que intentaremos aumentar la altura de la imagen y poner el valor de el ancho. En el offset de la altura ponemos los mismos valores que en el offset de anchura.
Abrimos la imagen y la bandera aparece
picoCTF{qu1t3_a_v13w_2020}

## Notas adicionales

## Referencias

