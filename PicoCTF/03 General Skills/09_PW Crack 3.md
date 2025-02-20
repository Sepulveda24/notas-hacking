Descripción
¿Puedes descifrar la contraseña para obtener la bandera?Descargue el comprobador de contraseñas [aquí](https://artifacts.picoctf.net/c/18/level3.py) y también necesitará la [bandera](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) encriptada y el [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) en el mismo directorio.Hay 7 contraseñas potenciales con 1 correcta. Puede encontrarlos examinando el script del comprobador de contraseñas.

Hints:
1.⁠ ⁠Para ver el archivo level3.hash.bin en el webshell, haga:`$ bvi level3.hash.bin`
2.To exit `bvi` type `:q` and press enter.
3.The `str_xor` function does not need to be reverse engineered for this challenge.

Solución 1

Con web shell

Sepulveda24-picoctf@webshell:~$ rm -rf *
Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.py
--2025-02-20 18:59:03--  https://artifacts.picoctf.net/c/18/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.93, 3.160.5.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py                                         100%[===========================================================================================================>]   1.31K  --.-KB/s    in 0s      

2025-02-20 18:59:03 (828 MB/s) - 'level3.py' saved [1337/1337]

Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
--2025-02-20 18:59:23--  https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.71, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc                               100%[===========================================================================================================>]      31  --.-KB/s    in 0s      

2025-02-20 18:59:24 (383 KB/s) - 'level3.flag.txt.enc' saved [31/31]

Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.hash.bin
--2025-02-20 18:59:30--  https://artifacts.picoctf.net/c/18/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.71, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin                                   100%[===========================================================================================================>]      16  --.-KB/s    in 0s      

2025-02-20 18:59:30 (5.86 MB/s) - 'level3.hash.bin' saved [16/16]

Sepulveda24-picoctf@webshell:~$ ls
level3.flag.txt.enc  level3.hash.bin  level3.py
Sepulveda24-picoctf@webshell:~$ nano level3.py
Sepulveda24-picoctf@webshell:~$ cat level3.flag.txt.enc 
B[ZZqfN_
        ]mTU\[UmS

X
 TDSepulveda24-picoctf@webshell:~$ nano level3.py
Sepulveda24-picoctf@webshell:~$ cat level3.hash.bin 
m`TA
    45&Sepulveda24-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: q
That password is incorrect
Sepulveda24-picoctf@webshell:~$ nano level3.py
Sepulveda24-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 8799
That password is incorrect
Sepulveda24-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 
That password is incorrect
Sepulveda24-picoctf@webshell:~$ nano level3.py
Sepulveda24-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: d3ab
That password is incorrect
Sepulveda24-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 1ea2
That password is incorrect
Sepulveda24-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: acaf
That password is incorrect
Sepulveda24-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
Sepulveda24-picoctf@webshell:~$ 
Notas adicionales

-------------

Referencias

https://webshell.picoctf.org