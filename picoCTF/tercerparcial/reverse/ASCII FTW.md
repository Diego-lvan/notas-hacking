


## Objetivo
This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program.You can download the file from [here](https://artifacts.picoctf.net/c/508/asciiftw).
## Solución
picoCTF{ASCII_IS_EASY_8960F0AF}
El proceso puede resumirse de esta manera:

1. Se desensambló el archivo "asciiftw" utilizando `objdump` y se guardó en un archivo de texto llamado "disassembled_asciiftw.txt" para evitar tener que ejecutar `objdump` repetidamente.

`objdump -d asciiftw > disassembled_asciiftw.txt`

2. Se utilizó `grep` para encontrar la función principal (`main`) y se extrajeron las 40 líneas siguientes usando el parámetro "-A".

`cat disassembled_asciiftw.txt | grep "<main>:" -A 40`

3. Se observó que los caracteres hexadecimales de la bandera tenían "movb" delante, por lo que se utilizó `grep` para filtrar solo las líneas que contenían "movb".


`cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb`

4. Se utilizó `cut` para extraer todo después del signo "$", que casi proporcionaba solo el hex.


`cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb | cut -d "$" -f2`

5. Luego, se utilizó `cut` nuevamente, esta vez usando la coma como delimitador, lo que proporcionó solo el hex deseado.


`cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb | cut -d "$" -f2 | cut -d "," -f1`

6. Para eliminar los caracteres de nueva línea, se utilizó `tr`.



`cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb | cut -d "$" -f2 | cut -d "," -f1 | tr -d "\n"`

7. Se usó `sed` para agregar un espacio antes de cada "0x", ya que es necesario para decodificar el hex.


`cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb | cut -d "$" -f2 | cut -d "," -f1 | tr -d "\n" | sed 's/0x/ 0x/g'`

8. Se eliminó el espacio inicial no deseado utilizando `sed`.


`cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb | cut -d "$" -f2 | cut -d "," -f1 | tr -d "\n" | sed 's/0x/ 0x/g' | sed 's/^ //g'`

9. Por último, se utilizó `xxd` para convertir el hex a ASCII y obtener la bandera.


`cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb | cut -d "$" -f2`
## Notas adicionales

## Referencias
