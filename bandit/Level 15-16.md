
## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.
## Datos de acceso
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
bandit15
## Solución
```
dit15@bandit:~$ echo "jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt" | openssl s_client -connect localhost:30001 -ign_eof
CONNECTED(00000003)

read R BLOCK
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

```
## Notas adicionales
- openssl s_client nos sirve para actuar como cliente y conectarte
- -ign-eof es para no cerrar la conexion hasta que me respondan
## Referencias
chatgpt