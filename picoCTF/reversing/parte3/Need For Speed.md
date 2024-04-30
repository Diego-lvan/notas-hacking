## Objetivo
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/27dd5548b14661f65ce3ac6a8a8f575b/need-for-speed).
## Solución
Lo desesamblamos con gdb y cambiamos 
Corremos handle SIGALRM ignore para que ignore el timpoe que ha transcurrido

SIGALRM is a signal in Unix-like operating systems that is sent to a process to indicate that a specified amount of real (wall-clock) time has elapsed



```
┌──(kali㉿kali)-[~/Desktop/pico]
└─$ gdb ./need-for-speed
Reading symbols from ./need-for-speed...
(No debugging symbols found in ./need-for-speed)
(gdb) handle SIGALRM ignore
Signal        Stop      Print   Pass to program Description
SIGALRM       No        No      No              Alarm clock
(gdb) r
Starting program: /home/kali/Desktop/pico/need-for-speed 
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".
Keep this thing over 50 mph!
============================

Creating key...
Finished
Printing flag:
PICOCTF{Good job keeping bus #1f2ac4ec speeding along!}
[Inferior 1 (process 26814) exited normally]
(gdb) 



```
## Notas adicionales

## Referencias
