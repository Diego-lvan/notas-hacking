## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de acceso
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit9
## Solución
```
	bandit9@bandit:~$ strings data.txt | grep ==
	x]T========== theG)"
	========== passwordk^
	========== is
	========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

```
## Notas adicionales
El comando strings se usa para extraer texto de archivos binarios
## Referencias
