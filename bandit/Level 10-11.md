## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos de acceso
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit10
## Solución
```
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ 

```
## Notas adicionales
- Base64 nos ayuda a codificar un texto
- Base64 -d nos ayuda a decodificar un texto

## Referencias
