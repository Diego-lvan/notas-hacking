## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/50009/` ([link](https://jupiter.challenges.picoctf.org/problem/50009/)) or http://jupiter.challenges.picoctf.org:50009. Do you think you can log us in? Try to see if you can login!
## Solución
Ingresar admin en el usuario
Hacer una inyeccion sql con el sig commando en el campo de password
```
' OR 1=1; --
```
## Notas adicionales
-- En sql es un comentario, por lo que forzamos a que se termine la query
## Referencias
