Descripción
The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.

Additional details will be available after launching your challenge instance.
Additional details will be available after launching your challenge instance.
Hints:
1.⁠ ⁠Where can you get some letters?


Solución 1

Con web shell y cyberchef

Sepulveda24-picoctf@webshell:~$ ssh -p 58328 ctf-player@mimas.picoctf.net
The authenticity of host '[mimas.picoctf.net]:58328 ([52.15.88.75]:58328)' can't be established.
ED25519 key fingerprint is SHA256:n/hDgUtuTTF85Id7k2fxmHvb6rrLrACHNM6xLZ46AqQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? y
Please type 'yes', 'no' or the fingerprint: yes
Warning: Permanently added '[mimas.picoctf.net]:58328' (ED25519) to the list of known hosts.
ctf-player@mimas.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1016-aws x86_64)

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

SansAlpha$ /*
bash: /bin: Is a directory

SansAlpha$ /*/???[!_]64 */*
/bin/base64: extra operand ‘blargh/flag.txt’
Try '/bin/base64 --help' for more information.

SansAlpha$ /*/???[!_]64 */????.*
cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV8zNmE2NzRjMH0=

SansAlpha$ 
Traceback (most recent call last):
  File "/usr/local/sansalpha.py", line 12, in <module>
    if user_in[-1] != "\n":
IndexError: string index out of range
Connection to mimas.picoctf.net closed.



cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV8zNmE2NzRjMH0=-------------Decodifique esto en cyberchef y me dio la bandera


picoCTF{proxies_all_the_way_25bbae9a}


Notas adicionales

--------------------


Referencias

https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnR3Y205NGFXVnpYMkZzYkY5MGFHVmZkMkY1WHpJMVltSmhaVGxoZlE9PQ 

