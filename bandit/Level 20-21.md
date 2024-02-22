## Objetivo

## Datos de acceso
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit20
## Solución
```
bandit20@bandit:~$ nc -lnvp 9999 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 135417
bandit20@bandit:~$ Listening on 0.0.0.0 9999
./suconnect 9999 
Connection received on 127.0.0.1 32800
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq

```
## Notas adicionales
- Para abrir un puerto es con nc -lnvp   
- & nos ayuda a mandarlo al segundo plano sin cerrar la terminal


## Referencias
