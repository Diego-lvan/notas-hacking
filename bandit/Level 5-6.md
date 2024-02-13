## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:
## Datos de acceso
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit5
## Solución
```
	bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere04  maybehere08  maybehere12  maybehere16
maybehere01  maybehere05  maybehere09  maybehere13  maybehere17
maybehere02  maybehere06  maybehere10  maybehere14  maybehere18
maybehere03  maybehere07  maybehere11  maybehere15  maybehere19
bandit5@bandit:~/inhere$ find -size 1033c -not -executable
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

```

## Notas adicionales
Aprendi que el comando file nos sirive para buscar archivos y que  tiene el argumento find que indica el tamaño y -not -executable para los archivos no ejecutables
## Referencias
