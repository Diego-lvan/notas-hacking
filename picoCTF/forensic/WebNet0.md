
## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
## Solución
picoCTF{nongshim.shrimp.crackers}
Abrimos el archivo de paquetes que nos dan, despues nos vamos a edit > preferences > protocols > tls > agregar llave por archivo. En este caso cargamos la llave que nos da el problema. Una vez desencriptado podemos buscar pico y la encontraremos

Otra solución: ssldump -r capture.pcap -k picopico.key -d | grep pico
## Notas adicionales

## Referencias
TLS es una forma de transportar datos encriptados
