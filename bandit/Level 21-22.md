## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.
## Datos de acceso
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
## Solución
```
bandit21@bandit:~$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:~$ nano /usr/bin/cronjob_bandit22.sh
Unable to create directory /home/bandit21/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit21@bandit:~$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff


```
## Notas adicionales
cron sirve para hacer tareas recurrentes en el sistema operativo
## Referencias
