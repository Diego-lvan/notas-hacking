


## Objetivo

Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).
## Solución
picoCTF{654874}

 0x9fe1a se pasa al registro del puntero base. En la línea <+22>, movemos este valor desde el puntero base en esta dirección a eax, y hemos encontrado nuestro valor almacenado en eax. En este punto, convertimos 0x9fe1a en decimal, y encontramos que representa el número 654874. 
## Notas adicionales

## Referencias
