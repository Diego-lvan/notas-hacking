
## Objetivo
Decode this [message](https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav) from the moon.
## Solución
instalar sstv para decodificar el audio a imagen 
para esto podemos instalar https://github.com/colaclanth/sstv
sstv -d ~/Desktop/pico/message.wav  -o ~/Desktop/pico/res.jpg
Haciendo esto obtenemos una imagen con la bandera 
## Notas adicionales
sstv nos permite decodificar un audio a una imagen 
## Referencias

