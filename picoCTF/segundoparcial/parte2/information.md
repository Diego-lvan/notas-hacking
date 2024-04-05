picoCTF{the_m3tadata_1s_modified}

## Objetivo
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/b4d62f6e431dc8e563309ea8c33a06b3/cat.jpg)
## Solución
Podemos ver que es una imagen valida, podemos checar su metadatos y en licesense vemos algo rato. Decodificamos eso de base64 y obtenemos la bandera

```
┌──(kali㉿kali)-[~/Desktop/pico]
└─$ echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 -d
picoCTF{the_m3tadata_1s_modified}                                                                                                                                                                                                                                            

```
## Notas adicionales

## Referencias
