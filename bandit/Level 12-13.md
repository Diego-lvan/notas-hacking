
## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)
## Datos de acceso
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit12
## Solución
```
	bandit12@bandit:/tmp/myname123$ xxd -r data.txt >> prueba.txt
bandit12@bandit:/tmp/myname123$ cat prueba.txt 
�h44�z��A����@=�h4hh������hd����������������9���1����������;,�
�����2�3d*58�~  �S�ZP^��luY��Br$�FP!%�s��h�?�)[=�h��O(B��2A���)�tZc��:�pã)�A�ˈ�0���΅A�yjeϢx,�(����z�E�+"�2�/�-��e"���^����t�j���$�d�@�dJơ'7\���$��m1c��#>�aԽ�EV��F��OCӐc@M�C���]��Y2^h8���D=��~	O�I��NDpF�+�|b#Jv�#�J��d�LފW$�Û�͖y�`
                                                                           �\&	��[�@*w�M�0θ��nr��C��`e$b�
                         ~�{���
                               ��`�<����a��?e:T���e�T4±b����)
                                                             �@ِ���x=bandit12@bandit:/tmp/myname123$ file prueba.txt 
prueba.txt: gzip compressed data, was "data2.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 573
bandit12@bandit:/tmp/myname123$ mv prueba.txt prueba.gz
bandit12@bandit:/tmp/myname123$ gzip -d prueba.gz 
bandit12@bandit:/tmp/myname123$ ls
data.txt  prueba
bandit12@bandit:/tmp/myname123$ file prueba 
prueba: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/myname123$ ls
data.txt  prueba
bandit12@bandit:/tmp/myname123$ mv prueba prueba.bz
bandit12@bandit:/tmp/myname123$ file prueba.bz 
prueba.bz: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/myname123$ bzip2 -d prueba.bz
bandit12@bandit:/tmp/myname123$ ls
data.txt  prueba
bandit12@bandit:/tmp/myname123$ file prueba
prueba: gzip compressed data, was "data4.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/myname123$ mv prueba prueba.gz
bandit12@bandit:/tmp/myname123$ gzip -d prueba.gz
bandit12@bandit:/tmp/myname123$ ls
data.txt  prueba
bandit12@bandit:/tmp/myname123$ file prueba 
prueba: POSIX tar archive (GNU)
bandit12@bandit:/tmp/myname123$ mv prueba prueba.tar
bandit12@bandit:/tmp/myname123$ tar -xf prueba.tar 
bandit12@bandit:/tmp/myname123$ file prueba.tar 
prueba.tar: POSIX tar archive (GNU)
bandit12@bandit:/tmp/myname123$ ls
data5.bin  data.txt  prueba.tar
bandit12@bandit:/tmp/myname123$ file data5.bin 
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/myname123$ mv data5.bin 
data5.bin   data.txt    prueba.tar  
bandit12@bandit:/tmp/myname123$ mv data5.bin data5.tar
bandit12@bandit:/tmp/myname123$ tar -xf data5.tar 
bandit12@bandit:/tmp/myname123$ ls
data5.tar  data6.bin  data.txt  prueba.tar
bandit12@bandit:/tmp/myname123$ file data6.bin 
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/myname123$ mv data6.bin data6.bz
bandit12@bandit:/tmp/myname123$ bzip2 -d data6.bz
bandit12@bandit:/tmp/myname123$ ls
data5.tar  data6  data.txt  prueba.tar
bandit12@bandit:/tmp/myname123$ file data6
data6: POSIX tar archive (GNU)
bandit12@bandit:/tmp/myname123$ mv data6 data6.tar
bandit12@bandit:/tmp/myname123$ tar -xf data6.tar 
bandit12@bandit:/tmp/myname123$ ls
data5.tar  data6.tar  data8.bin  data.txt  prueba.tar
bandit12@bandit:/tmp/myname123$ file data8ffff
data8ffff: cannot open `data8ffff' (No such file or directory)
bandit12@bandit:/tmp/myname123$ file data8
data8: cannot open `data8' (No such file or directory)
bandit12@bandit:/tmp/myname123$ file data8.bin 
data8.bin: gzip compressed data, was "data9.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/myname123$ mv data8.bin data8.gz
bandit12@bandit:/tmp/myname123$ gzip -d data8.gz 
bandit12@bandit:/tmp/myname123$ ls
data5.tar  data6.tar  data8  data.txt  prueba.tar
bandit12@bandit:/tmp/myname123$ file data8
data8: ASCII text
bandit12@bandit:/tmp/myname123$ cat data8
wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
## Notas adicionales
Aprendi a descomprimir las diferentes extension para la mayoria se usa el parametro -d
Para tar se usa -xf
## Referencias
