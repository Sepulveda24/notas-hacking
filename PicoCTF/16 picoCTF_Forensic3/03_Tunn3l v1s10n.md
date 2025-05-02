Descripción
Encontramos este [archivo](https://mercury.picoctf.net/static/7b2d7c26630e977197022d0af09e3aeb/tunn3l_v1s10n). Recupera la bandera.

Hints:
1.⁠ ⁠Es extraño que no se muestre bien...

Solución 1

Con Terminal de linux
                                                                             ┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Desktop  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ ls
 firefox-esr  'Parallels Shared Folders'   Retos
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ cd Retos  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ ^[[200~wget https://mercury.picoctf.net/static/7b2d7c26630e977197022d0af09e3aeb/tunn3l_v1s10n~
zsh: bad pattern: ^[[200~wget
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ wget https://mercury.picoctf.net/static/7b2d7c26630e977197022d0af09e3aeb/tunn3l_v1s10n
--2025-05-02 15:33:15--  https://mercury.picoctf.net/static/7b2d7c26630e977197022d0af09e3aeb/tunn3l_v1s10n
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2893454 (2.8M) [application/octet-stream]
Saving to: ‘tunn3l_v1s10n’

tunn3l_v1s10n       100%[================>]   2.76M  6.97MB/s    in 0.4s    

2025-05-02 15:33:20 (6.97 MB/s) - ‘tunn3l_v1s10n’ saved [2893454/2893454]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ ls
binwalk  dolls.jpg  myenv  tunn3l_v1s10n
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ hexeditor tunn3l_v1s10n.bmp
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ mv tunn3l_v1s10n tunn3l_v1s10n.bmp
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ hexeditor tunn3l_v1s10n.bmp       

zsh: suspended  hexeditor tunn3l_v1s10n.bmp
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ hexeditor tunn3l_v1s10n.bmp
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ hexeditor tunn3l_v1s10n.bmp       
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ open tunn3l_v1s10n.bmp 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ 

Notas adicionales

--------------------
picoCTF{qu1t3_a_v13w_2020}

Referencias

https://en.wikipedia.org/wiki/BMP_file_format