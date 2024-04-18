## Objetivo
This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://jupiter.challenges.picoctf.org/static/c695ee23309d453a3ef369c34cc1bccb/VaultDoor4.java)
## Solución
Agregamos lo siguiente para convertir a ascci

jU5t_4_bUnCh_0f_bYt3s_8f4a6cbf3b

```
StringBuilder result = new StringBuilder();

for (byte b : myBytes) {

result.append((char) b);

}

  

String charString = result.toString();

System.out.println(charString);
```
## Notas adicionales

## Referencias


jU5t_4_bUnCh_0f_bYt3s_8f4a6cbf3b