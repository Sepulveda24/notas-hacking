Descripción
Using a Secure Shell (SSH) is going to be pretty important.

Additional details will be available after launching your challenge instance.


Hints:
1.⁠ ⁠[https://linux.die.net/man/1/ssh](https://linux.die.net/man/1/ssh)
2.You can try logging in 'as' someone with `<user>`@titan.picoctf.net
3.How could you specify the port?
4.Remember, passwords are hidden when typed into the shell

Solución 1

Con web shell


Sepulveda24-picoctf@webshell:~$ ssh ctf-player@titan.picoctf.net -p 52319
The authenticity of host '[titan.picoctf.net]:52319 ([3.139.174.234]:52319)' can't be established.
ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[titan.picoctf.net]:52319' (ED25519) to the list of known hosts.
ctf-player@titan.picoctf.net's password: 
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_3e293eea}
Connection to titan.picoctf.net closed.
Sepulveda24-picoctf@webshell:~$ 


Notas adicionales

-------------

Referencias

https://webshell.picoctf.org