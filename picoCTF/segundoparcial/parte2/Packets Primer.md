## Objetivo
Download the packet capture file and use packet analysis software to find the flag.

- [Download packet capture](https://artifacts.picoctf.net/c/196/network-dump.flag.pcap)
## Solución
```
└─$ strings network-dump.flag.pcap 
k&Nar
n#('
k&Na
k&Na`
n#('
k&Na;
n#('
p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ 0 1 b 0 a 0 d 6 }
k&Naa
ep&Na(
p&NaX
p&Na28
p&Na

```

picoCTF{p4ck37_5h4rk_01b0a0d6}

## Notas adicionales

## Referencias
