Descripción
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/static)? This [BASH script](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/ltdis.sh)might help!

Hints:
(none)
Solución 1

Con web shell
Sepulveda24-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/static
--2025-02-18 18:30:42--  https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static'

static                                            100%[===========================================================================================================>]   8.18K  --.-KB/s    in 0s      

2025-02-18 18:30:42 (228 MB/s) - 'static' saved [8376/8376]

Sepulveda24-picoctf@webshell:~$ ls
README.txt  static  strings  warm
Sepulveda24-picoctf@webshell:~$ chmod +x static
Sepulveda24-picoctf@webshell:~$ ls
README.txt  static  strings  warm
Sepulveda24-picoctf@webshell:~$ ./static
Oh hai! Wait what? A flag? Yes, it's around here somewhere!
Sepulveda24-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_f6c48608}



Notas adicionales

------------


Referencias

https://webshell.picoctf.org