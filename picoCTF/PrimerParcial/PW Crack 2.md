## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
## Solución
```
if( user_pw == chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) ):
```
convertir los valores decimales a ascii y de ahi a char y unirlos

```
	Please enter correct password for flag: de76
	Welcome back... your flag, user:
	picoCTF{tr45h_51ng1ng_489dea9a}

```

## Notas adicionales

## Referencias
