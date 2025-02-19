Descripción
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm)has extraordinarily helpful information...

Hints:
1.⁠ This program will only work in the webshell or another Linux computer.
2.To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm`
3.Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
4.-h and --help are the most common arguments to give to programs to get more information from them!
5.Not every program implements help features like -h and --help.


Solución 1

Con web shell

Sepulveda24-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
--2025-02-18 18:24:19--  https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                            100%[======================================================>]  10.68K  --.-KB/s    in 0s      

2025-02-18 18:24:19 (405 MB/s) - 'warm' saved [10936/10936]

Sepulveda24-picoctf@webshell:~$ ls
README.txt  strings  warm
Sepulveda24-picoctf@webshell:~$ file warm
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=3181a501366281ab5eba1c41e54a1f40800e3966, with debug_info, not stripped
Sepulveda24-picoctf@webshell:~$ chmod +x warm
Sepulveda24-picoctf@webshell:~$ ls
README.txt  strings  warm
Sepulveda24-picoctf@webshell:~$ . /warm
-bash: /warm: No such file or directory
Sepulveda24-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
Sepulveda24-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}
Sepulveda24-picoctf@webshell:~$ 




Notas adicionales

------------

Referencias

https://webshell.picoctf.org