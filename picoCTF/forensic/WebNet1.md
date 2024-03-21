



## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Solución
Como el problema anterior, necesitamos cargar la key dentro de wireshark, en este caso la bandera no esta en texto plano, pero podemos ver que hubo descarga de archivos.
Vamos a file > Objects > Http y descargamos la imagen. A la imagen le aplicamos strings y un grep y obtenemos la bandera


picoCTF{honey.roasted.peanuts}

## Notas adicionales

## Referencias

