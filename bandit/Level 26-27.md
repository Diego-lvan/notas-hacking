## Objetivo
Good job getting a shell! Now hurry and grab the password for bandit27!
## Datos de acceso
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
## Solución
Igual que en el nivel anterior se necesita hacer la terminal pequeña y abrir vim
Ejecutar los siguientes comandos:
```:set shell=/bin/bash 
	:shell

```

```
bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$  echo 'cat /etc/bandit_pass/bandit27' > /tmp/getpass27.sh
bandit26@bandit:~$ chmod a+x /tmp/getpass27.sh
bandit26@bandit:~$ ./bandit27-do /tmp/getpass27.sh
cat: /etc/bandit_pass/bandit27: Permission denied
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$ 


```

## Notas adicionales

## Referencias
