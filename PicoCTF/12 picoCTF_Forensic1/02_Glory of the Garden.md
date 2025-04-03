Descripción
This [garden](https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg) contains more than it seems.

Hints:
1.⁠ ⁠What is a hex editor?

Solución 1

Con inspeccion de elemento

(parallels㉿kali-linux-2022-2)-[~]
└─$ wget https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg
--2025-04-02 23:43:38--  https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2295192 (2.2M) [application/octet-stream]
Saving to: ‘garden.jpg’

garden.jpg          100%[================>]   2.19M  3.69MB/s    in 0.6s    

2025-04-02 23:43:39 (3.69 MB/s) - ‘garden.jpg’ saved [2295192/2295192]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 cookies.txt   Downloads    Music      server.py   Videos
 Desktop       flag.png     Pictures   Templates   webshell.php
 Documents     garden.jpg   Public    '~.venv'     webshell.png.php
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ open garden.jpg 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ hexeditor garden.jpg 

picoCTF{more_than_m33ts_the_3y3657BaB2C}


Notas adicionales

--------------------


Referencias

https://hexed.it