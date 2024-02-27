## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
## Datos de acceso
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
bandit23
## Solución
```
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ nano bandit24_pass.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/tmp.Bd906nDXgT$ nano bandit24_pass.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/tmp.Bd906nDXgT$ ls
bandit24_pass.sh
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ hmod +rx bandit24_pass.sh 
Command 'hmod' not found, did you mean:
  command 'kmod' from deb kmod (29-1ubuntu1)
  command 'qmod' from deb gridengine-client (8.1.9+dfsg-10build1)
  command 'chmod' from deb coreutils (8.32-4.1ubuntu1)
  command 'jmod' from deb openjdk-11-jdk-headless (11.0.20.1+1-0ubuntu1~22.04)
  command 'jmod' from deb openjdk-17-jdk-headless (17.0.8.1+1~us1-0ubuntu1~22.04)
  command 'jmod' from deb openjdk-18-jdk-headless (18.0.2+9-2~22.04)
  command 'jmod' from deb openjdk-19-jdk-headless (19.0.2+7-0ubuntu3~22.04)
  command 'mod' from deb monodoc-base (6.8.0.105+dfsg-3.2)
Try: apt install <deb name>
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ chmod +rx bandit24_pass.sh 
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ chmod 777 /tmp/tmp.Bd906nDXgT
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ touch password
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ chmod +rwx password 
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ ls -la
total 408
drwxrwxrwx   2 bandit23 bandit23   4096 Feb 27 04:36 .
drwxrwx-wt 638 root     root     405504 Feb 27 04:36 ..
-rwxrwxr-x   1 bandit23 bandit23     74 Feb 27 04:35 bandit24_pass.sh
-rwxrwxr-x   1 bandit23 bandit23      0 Feb 27 04:36 password
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ cp bandit24_pass.sh /var/spool/bandit24/bandit24_pass.sh
cp: cannot create regular file '/var/spool/bandit24/bandit24_pass.sh': Operation not permitted
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ cp bandit24_pass.sh /var/spool/bandit24/bandit24_pass.sh
cp: cannot create regular file '/var/spool/bandit24/bandit24_pass.sh': Operation not permitted
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ chmod +rx bandit24_pass.sh 
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ chmod 777 /tmp/tmp.Bd906nDXgT
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ ls
bandit24_pass.sh  password
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ hmod +rwx password 
Command 'hmod' not found, did you mean:
  command 'kmod' from deb kmod (29-1ubuntu1)
  command 'chmod' from deb coreutils (8.32-4.1ubuntu1)
  command 'jmod' from deb openjdk-11-jdk-headless (11.0.20.1+1-0ubuntu1~22.04)
  command 'jmod' from deb openjdk-17-jdk-headless (17.0.8.1+1~us1-0ubuntu1~22.04)
  command 'jmod' from deb openjdk-18-jdk-headless (18.0.2+9-2~22.04)
  command 'jmod' from deb openjdk-19-jdk-headless (19.0.2+7-0ubuntu3~22.04)
  command 'qmod' from deb gridengine-client (8.1.9+dfsg-10build1)
  command 'mod' from deb monodoc-base (6.8.0.105+dfsg-3.2)
Try: apt install <deb name>
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ chmod +rwx password 
bandit23@bandit:/tmp/tmp.Bd906nDXgT$ cp bandit24_pass.sh /var/spool/bandit24/bandit24_pass.sh
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
```
## Notas adicionales

## Referencias
