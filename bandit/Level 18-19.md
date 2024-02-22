## Objetivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**
## Datos de acceso
hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
## Solución
```
diego@diego-Laptop:~/Desktop/IS/seguridad$ ssh  bandit18@bandit.labs.overthewire.org -p 2220  cat readme
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password: 
awhqfNnAbc1naukrpqDYcF95h7HoMTrC

```
## Notas adicionales
Puedes poner comandos que se ejecutan al inicio en .bashsrc  
Puede poner un comando al final de la conexion para que se ejecute antes de salir
## Referencias
