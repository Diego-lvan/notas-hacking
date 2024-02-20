## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
## Datos de acceso
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit 14
## Solución
```
bandit14@bandit:~$ echo fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq | nc localhost 30000
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

```
## Notas adicionales
Aprendi a enviar datos a un puerto con el comando nc server port
## Referencias
