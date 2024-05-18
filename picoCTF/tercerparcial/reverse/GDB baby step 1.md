


## Objetivo
Can you figure out what is in the `eax` register at the end of the `main` function? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Disassemble [this](https://artifacts.picoctf.net/c/512/debugger0_a).
## Solución
usamos gdb 

```
gdb debugger0_a
```

```
 set disassembly-flavor intel
```


```bash
disassemble main
```
 A partir del código desensamblado, vemos que el número 0x86342 se mueve a este registro.
```
print(int(0x86342))
```
## Notas adicionales

## Referencias
