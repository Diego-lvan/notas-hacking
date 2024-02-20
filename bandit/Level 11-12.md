
# Level X

## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Datos de acceso
bandit11
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

## Solución
```
	bandit11@bandit:~$ cat data.txt | tr '[a-z][A-Z]' '[n-za-m][N-ZA-M]'
	The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

```
## Notas adicionales
	Aprendi a rotar caracteres con la funcion tr 
## Referencias
https://askubuntu.com/questions/1085069/how-can-i-decode-a-file-where-each-letter-has-been-replaced-with-the-letter-13-l