## Objetivo
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.
## Datos de acceso
p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
bandit25
## Solución

```
	bandit25@bandit:~$ cat /etc/passwd | grep bandit26  
bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext  
bandit25@bandit:~$

bandit25@bandit:~$ cat /usr/bin/showtext  
#!/bin/shexport TERM=linuxmore ~/text.txt  
exit 0  
bandit25@bandit:~$

```
Se tiene que rescalar la ventana y hacerla pequeña, con eso puedes entrar por ssh.
Una vez dentro puedes ejecutar vim con 'v' y dentro de vim abrir el archivo de la pwd del usuario
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
## Notas adicionales

## Referencias
