## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:
## Datos de acceso
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
bandit6
## Solución
```
bandit6@bandit:~$ find /  -user bandit7 -group bandit6 -size 33c 2>/dev/null

```
## Notas adicionales
Use el comando file para buscar el archivo, con el parametro group para buscar el grupo y user, 2 es para las salidas de error y lo mando a null 

## Referencias
