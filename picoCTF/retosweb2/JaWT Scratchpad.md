## Objetivo
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/58210/` or http://jupiter.challenges.picoctf.org:58210
## Solución
descargar [JohnTheRipper](https://github.com/openwall/john). en linux
En rockyou se encuentran las contaseñas mas comunes
Haciendo un ataque de fuerza bruta en las contraseñas mas comunes con el 
```
John jwt.txt --format=HMAC-SHA256 --wordlist-/home/Downloads/rockyou.txt
```
Esto nos devolvera la clave de JWT y con esto podemos ir a https://jwt.io/ y poner el token que nos devolvio al logearnos, pero cambiamos el usuario a admin y la clave JWT en secret.
Con esto tenemos un token valido lo podemos añadir a un header y nos dará acceso.

## Notas adicionales
- JWT
	- Header: The first section consists of a header which basically tells us which type of algorithm to use
	- Payload: The second section is the payload which is also base64URL encoded and it pretty much holds the name of the user
	- Signature: This section validates the token and checks if the token has been tampered.
## Referencias
https://infosecwriteups.com/jawt-scratchpad-picoctf-93766d81fd8e
https://jwt.io/