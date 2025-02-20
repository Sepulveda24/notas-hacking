Descripción
¿Puedes descifrar la contraseña para obtener la bandera?Descargue el comprobador de contraseñas [aquí](https://artifacts.picoctf.net/c/10/level1.py) y también necesitará la [bandera](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) cifrada en el mismo directorio.

---

Hints:
1.⁠ ⁠Para ver el archivo en el webshell, haga:`$ nano level1.py`
2.Para salir de `nano`, presione Ctrl y x y siga las indicaciones en pantalla.
3.The `str_xor` function does not need to be reverse engineered for this challenge.


Solución 1

Con web shell

Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/10/level1.py
--2025-02-20 18:11:08--  https://artifacts.picoctf.net/c/10/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.42, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py                                         100%[===========================================================================================================>]     876  --.-KB/s    in 0s      

2025-02-20 18:11:08 (1.01 GB/s) - 'level1.py' saved [876/876]

Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
--2025-02-20 18:11:14--  https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.93, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc                               100%[===========================================================================================================>]      30  --.-KB/s    in 0s      

2025-02-20 18:11:15 (1010 KB/s) - 'level1.flag.txt.enc' saved [30/30]

Sepulveda24-picoctf@webshell:~$ ls
level1.flag.txt.enc  level1.py
Sepulveda24-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 1
That password is incorrect
Sepulveda24-picoctf@webshell:~$ cat level1.flag.txt.enc 
FPR
   umw
iK
_i
  UDSepulveda24-picoctf@webshell:~$ nano level1.py 
Sepulveda24-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}
Sepulveda24-picoctf@webshell:~$ 
Notas adicionales

-------------

Referencias

https://webshell.picoctf.org