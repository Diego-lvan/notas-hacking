
## Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/51d68e61bb41207a55f24e753f07c5a3/values)
## Solución
```
└─$ cat values    
Decrypt my super sick RSA:
c: 62324783949134119159408816513334912534343517300880137691662780895409992760262021
n: 1280678415822214057864524798453297819181910621573945477544758171055968245116423923
e: 65537                                                                                                                                                                       

```

```
p = 1899107986527483535344517113948531328331

q = 674357869540600933870145899564746495319033

n = p * q

tn = (p-1) * (q-1)

e = 65537

d = pow(e, -1, tn)

c = 62324783949134119159408816513334912534343517300880137691662780895409992760262021

m = pow(c,d,n)

print(bytes.fromhex(hex(m)[2:]).decode('utf-8'))
```

## Notas adicionales

## Referencias
