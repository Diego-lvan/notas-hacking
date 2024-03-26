## Objetivo
Can you handle APKs?Download the android apk [here](https://artifacts.picoctf.net/c_titan/140/mobpsycho.apk).
## Solución
```
┌──(kali㉿kali)-[~/Desktop/pico]
└─$ unzip mobpsycho.apk | grep flag          
replace res/anim/abc_fade_in.xml? [y]es, [n]o, [A]ll, [N]one, [r]ename: A
  inflating: res/color/flag.txt      
                                                                                                                              
┌──(kali㉿kali)-[~/Desktop/pico]
└─$ cat res/color/flag.txt                   
7069636f4354467b6178386d433052553676655f4e5838356c346178386d436c5f35653637656135657d
                                                                                                                              
┌──(kali㉿kali)-[~/Desktop/pico]
└─$ cat res/color/flag.txt | grep xxd -r -p
grep: invalid option -- 'p'
Usage: grep [OPTION]... PATTERNS [FILE]...
Try 'grep --help' for more information.
                                                                                                                              
┌──(kali㉿kali)-[~/Desktop/pico]
└─$ cat res/color/flag.txt | xxd -r -p     
picoCTF{ax8mC0RU6ve_NX85l4ax8mCl_5e67ea5e}
```
## Notas adicionales

## Referencias
