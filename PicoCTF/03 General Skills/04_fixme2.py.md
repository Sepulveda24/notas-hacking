Descripción
Arregle el error de sintaxis en el script de Python para imprimir la bandera.[Descargar script de Python](https://artifacts.picoctf.net/c/4/fixme2.py)

Hints:
1.⁠ ⁠¿La igualdad y la asignación son el mismo símbolo?
2.Para ver el archivo en el webshell, haga:`$ nano fixme2.py`
3.Para salir de `nano`, presione Ctrl y x y siga las indicaciones en pantalla.
4The `str_xor` function does not need to be reverse engineered for this challenge.

Solución 1

Con web shell

Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/4/fixme2.py
--2025-02-20 18:05:15--  https://artifacts.picoctf.net/c/4/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.18, 3.160.5.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                         100%[===========================================================================================================>]   1.00K  --.-KB/s    in 0s      

2025-02-20 18:05:15 (595 MB/s) - 'fixme2.py' saved [1029/1029]

Sepulveda24-picoctf@webshell:~$ ls
README.txt  convertme.py  fixme1.py  fixme2.py
Sepulveda24-picoctf@webshell:~$ python fixme2.py 
  File "/home/Sepulveda24-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
Sepulveda24-picoctf@webshell:~$ nano fixme2.py 
Sepulveda24-picoctf@webshell:~$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
Sepulveda24-picoctf@webshell:~$ 

Notas adicionales

-------------

Referencias

https://webshell.picoctf.org