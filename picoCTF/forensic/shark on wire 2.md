## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.
## Solución
Lo abrimos en wireshark
Vemos algo raro, todos lo paquetes van al puerto 22 podemos hacer un filtro con udp.port == 22 para ver los los udp del puerto 22. 
El origen del puerto de cada mensaje empieza por 5 y tiene 3 digitos. Estos 3 digitos son codigos ascii, podemos meter todos esto numero en algo como cyberchef para obtener el valor
112 105 99 111 67 84 70 123 112 49 76 76 102 51 114 51 100 95 100 97 116 97 95 118 49 97 95 115 116 51 103 48 125
picoCTF{p1LLf3r3d_data_v1a_st3g0}


## Notas adicionales

## Referencias
