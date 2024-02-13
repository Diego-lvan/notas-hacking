## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de acceso
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit8
## Solución
```
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t

```

## Notas adicionales
aprendi que uniq solo elimina las entradas consecutivas por lo que tuve que ordenarlo y a parte usar -u especifica que solo se deben mostrar las líneas únicas
## Referencias
