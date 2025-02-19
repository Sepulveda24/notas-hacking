Descripción
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?

Hints:
1.⁠ ⁠[strings](https://linux.die.net/man/1/strings)

Solución 1

Con web shell
Sepulveda24-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
--2025-02-19 01:02:27--  https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings'

strings                                           100%[===========================================================================================================>] 757.84K  1.87MB/s    in 0.4s    

2025-02-19 01:02:28 (1.87 MB/s) - 'strings' saved [776032/776032]

Sepulveda24-picoctf@webshell:~$ ls
README.txt  enc_flag  strings
Sepulveda24-picoctf@webshell:~$ file strings
strings: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=0cdedfba33422d235dba8c90e00fb77b235f1ff8, not stripped
Sepulveda24-picoctf@webshell:~$ ls -la
total 800
drwxr-xr-x 4 Sepulveda24-picoctf Sepulveda24-picoctf   4096 Feb 19 01:02 .
drwxr-xr-x 3 root                root                    33 Feb 11 18:26 ..
-rw------- 1 Sepulveda24-picoctf Sepulveda24-picoctf   1435 Feb 18 19:51 .bash_history
-rw-r--r-- 1 Sepulveda24-picoctf Sepulveda24-picoctf    220 Feb 11 18:26 .bash_logout
-rw-r--r-- 1 Sepulveda24-picoctf Sepulveda24-picoctf   3771 Feb 11 18:26 .bashrc
drwxrwxr-x 3 Sepulveda24-picoctf Sepulveda24-picoctf     19 Feb 18 19:26 .local
-rw-r--r-- 1 Sepulveda24-picoctf Sepulveda24-picoctf    807 Feb 11 18:26 .profile
-rw------- 1 Sepulveda24-picoctf Sepulveda24-picoctf    367 Feb 12 00:50 .python_history
drwx------ 2 Sepulveda24-picoctf Sepulveda24-picoctf     48 Feb 18 18:51 .ssh
-rw-rw-r-- 1 Sepulveda24-picoctf Sepulveda24-picoctf    167 Feb 19 01:02 .wget-hsts
-rw-r--r-- 1 root                root                  4443 Feb 19 01:02 README.txt
-rw-rw-r-- 1 Sepulveda24-picoctf Sepulveda24-picoctf    349 Mar 16  2023 enc_flag
-rw-rw-r-- 1 Sepulveda24-picoctf Sepulveda24-picoctf 776032 Oct 26  2020 strings
Sepulveda24-picoctf@webshell:~$ ls
README.txt  enc_flag  strings
Sepulveda24-picoctf@webshell:~$ chmod +x strings
Sepulveda24-picoctf@webshell:~$ ls
README.txt  enc_flag  strings
Sepulveda24-picoctf@webshell:~$ ./strings
Maybe try the 'strings' function? Take a look at the man page
Sepulveda24-picoctf@webshell:~$ man strings
Sepulveda24-picoctf@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_7f766a23}



Notas adicionales

--------------

Referencias

https://webshell.picoctf.org