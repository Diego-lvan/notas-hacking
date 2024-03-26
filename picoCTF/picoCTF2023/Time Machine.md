## Objetivo
What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/160/challenge.zip)
## Solución
```
┌──(kali㉿kali)-[~/Desktop/pico/drop-in]
└─$ cat message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...                                                                                                                              
┌──(kali㉿kali)-[~/Desktop/pico/drop-in]
└─$ git status                                           
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        challenge.zip
        drop-in/
        flag.py

nothing added to commit but untracked files present (use "git add" to track)
                                                                                                                              
┌──(kali㉿kali)-[~/Desktop/pico/drop-in]
└─$ git log   
commit 89d296ef533525a1378529be66b22d6a2c01e530 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:22 2024 +0000

    picoCTF{t1m3m@ch1n3_186cd7d7}


```
## Notas adicionales

## Referencias
