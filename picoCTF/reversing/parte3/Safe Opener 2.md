


## Objetivo
What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/290/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
## Solución
Podemos hacer un strings al archivo .class
```
	┌──(kali㉿kali)-[~/Desktop/pico]
└─$ strings SafeOpener.class | grep pico
,picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}
                                                 
```
## Notas adicionales

## Referencias



