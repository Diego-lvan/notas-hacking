


## Objetivo
Can you figure out what is in the `eax` register at the end of the `main` function? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Debug [this](https://artifacts.picoctf.net/c/520/debugger0_b).
## Solución
picoCTF{307019}
Comienza estableciendo un punto de interrupción en la función 'main' utilizando

```
break main
```
A continuación, para obtener una imagen más clara del código ensamblador, establezca el diseño en ensamblador utilizando

```
layout asm
```

y luego ejecuta el programa usando el comando

```
run
```
La ejecución se detiene en la primera instrucción de 'main', pero necesitamos el contenido del registro EAX al final de la función. La función termina con la instrucción 'ret' en la dirección 0x401142.

Establezca el punto de interrupción en 0x401142 utilizando el comando:

```
break *0x401142
```
con el asterisco significando una dirección de memoria.
Ahora, dejemos que el programa siga su curso con el comando (abreviatura de "continue")

```
c
```
Como verás, el puntero apunta ahora a la dirección deseada. Si no estás seguro, puedes comprobar el contenido del registro del puntero de instrucción (RIP) mediante:

```
info registros rip
```

```
print/d $eax
```


## Notas adicionales

## Referencias
