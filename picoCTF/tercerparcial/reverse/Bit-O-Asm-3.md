


## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt).
## Solución
picoCTF{2619997}
```
>>> a=int("0x9fe1a",16) 
>>>  b=int("0x4",16)
>>> a*=b        
>>> c=int("0x1f5",16)   
>>> a+=c
>>> a
>>>  2619997       

```


## Notas adicionales

## Referencias
