


## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt).
## Solución
```
push rbp en <+4>: Empuja el puntero base a la pila.
mov rbp,rsp a <+5>: Mueve el puntero de la pila al puntero base.
mov DWORD PTR [rbp-0x4],edi en <+8>: Mueve el valor de edi a la posición de memoria [rbp-0x4].
mov QWORD PTR [rbp-0x10],rsi a <+11>: Mueve el valor de rsi a la posición de memoria [rbp-0x10].
mov eax,0x30 en <+15>: Mueve el valor inmediato 0x30 (48 en decimal) al registro eax.
pop rbp en <+20>: Restaura el puntero base de la pila.
ret en <+21>: Retorno de la función.
La instrucción clave que establece el valor de eax es:

<+15>: mov eax,0x30
picoCTF{48}

```

## Notas adicionales

## Referencias
