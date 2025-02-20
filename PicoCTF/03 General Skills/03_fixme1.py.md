Descripción
Arregla el error de sintaxis en este script de Python para imprimir la bandera.[Descargar script de Python](https://artifacts.picoctf.net/c/25/fixme1.py)

Hints:
1.⁠ ⁠La sangría es muy significativa en Python
2.Para ver el archivo en el webshell, haga:`$ nano fixme1.py`
3.Para salir de `nano`, presione Ctrl y x y siga las indicaciones en pantalla.
4.The `str_xor` function does not need to be reverse engineered for this challenge.

Solución 1

Con web shell


Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/25/fixme1.py
--2025-02-20 17:58:22--  https://artifacts.picoctf.net/c/25/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.18, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py                                         100%[===========================================================================================================>]     837  --.-KB/s    in 0s      

2025-02-20 17:58:22 (25.3 MB/s) - 'fixme1.py' saved [837/837]

Sepulveda24-picoctf@webshell:~$ ls
README.txt  convertme.py  fixme1.py
Sepulveda24-picoctf@webshell:~$ nano fixme1.py 
Sepulveda24-picoctf@webshell:~$ python fixme1.py 
  File "/home/Sepulveda24-picoctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
Sepulveda24-picoctf@webshell:~$ nano fixme1.py 
Sepulveda24-picoctf@webshell:~$ python
Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import random
>>> 
>>> 
>>> 
>>> def str_xor(secret, key):
...     #extend key to secret length
...     new_key = key
...     i = 0
...     while len(new_key) < len(secret):
...         new_key = new_key + key[i]
...         i = (i + 1) % len(key)        
...     return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
... 
>>> 
>>> flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) + chr(0x0b) + chr(0x1a) + chr(0x5a) + chr(0x>
  File "<stdin>", line 1
    flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) + chr(0x0b) + chr(0x1a) + chr(0x5a) + chr(0x>
                                                                                                                                                                                                        ^
SyntaxError: invalid hexadecimal literal
>>> 
>>>   
>>> flag = str_xor(flag_enc, 'enkidu')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'flag_enc' is not defined
>>> flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) + chr(0x0b) + chr(0x1a) + chr(0x5a) + chr(0x>exit(9
  File "<stdin>", line 1
    flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) + chr(0x0b) + chr(0x1a) + chr(0x5a) + chr(0x>exit(9
                                                                                                                                                                                                        ^
SyntaxError: invalid hexadecimal literal
>>> 
KeyboardInterrupt
>>> exit()
Sepulveda24-picoctf@webshell:~$ nano fixme1.py 
Sepulveda24-picoctf@webshell:~$ python fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
Sepulveda24-picoctf@webshell:~$ 

Notas adicionales

-------------

Referencias

https://webshell.picoctf.org