Descripción

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.

Hints:
1.⁠ ⁠Does that encoding look familiar?
2.The `str_xor` function does not need to be reverse engineered for this challenge.

Solución 1

Con web shell y cyberchef

Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.py
--2025-02-20 18:34:02--  https://artifacts.picoctf.net/c/15/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.71, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py                                         100%[===========================================================================================================>]     914  --.-KB/s    in 0s      

2025-02-20 18:34:02 (50.4 MB/s) - 'level2.py' saved [914/914]

Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
--2025-02-20 18:34:09--  https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.42, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc                               100%[===========================================================================================================>]      31  --.-KB/s    in 0s      

2025-02-20 18:34:09 (14.2 MB/s) - 'level2.flag.txt.enc' saved [31/31]

Sepulveda24-picoctf@webshell:~$ ls
README.txt  level1.flag.txt.enc  level1.py  level2.flag.txt.enc  level2.py
Sepulveda24-picoctf@webshell:~$ nano level2.py 
Sepulveda24-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
Sepulveda24-picoctf@webshell:~$ 

Usando cyberchef https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=Y2hyKDB4MzMpICsgY2hyKDB4MzkpICsgY2hyKDB4NjMpICsgY2hyKDB4NjUp&oeol=FF

'''
Input: chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65)
Recipe: from hex
Output: 39ce
'''



Notas adicionales

-------------

Referencias

https://webshell.picoctf.org

 https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=Y2hyKDB4MzMpICsgY2hyKDB4MzkpICsgY2hyKDB4NjMpICsgY2hyKDB4NjUp&oeol=FF
