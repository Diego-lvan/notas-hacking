


## Objetivo
I wonder what this really is... [enc](https://mercury.picoctf.net/static/2b4cea9b07db22bf4f933fddd1b8caa9/enc) `''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`
## Solución
picoCTF{16_bits_inst34d_of_8_04c0760d}
Usamos el sig script que decofica de utf-8
```
encoded_flag = open("enc").read()  
flag = ""  
for i in range(0, len(encoded_flag)):  
character1 = chr((ord(encoded_flag[i]) >> 8))  
character2 = chr(encoded_flag[i].encode('utf-16be')[-1])  
flag += character1  
flag += character2  
  
print("Flag: " + flag)
```
## Notas adicionales

## Referencias
