Descripción
How to automate tasks to run at intervals on linux servers?

Additional details will be available after launching your challenge instance.

¿Cómo automatizar las tareas para que se ejecuten a intervalos en servidores Linux?Usa ssh para conectarte a este servidor:

```
Server: saturn.picoctf.net
Port: 49261
Username: picoplayer 
Password: 5wf1w1hVxt
```
Hints:
1.⁠ ⁠(None)


Solución 1

Con web shell


Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/136/challenge.zip
--2025-02-20 21:16:41--  https://artifacts.picoctf.net/c_titan/136/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.18, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19196 (19K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                     100%[===========================================================================================================>]  18.75K  --.-KB/s    in 0.007s  

2025-02-20 21:16:41 (2.57 MB/s) - 'challenge.zip' saved [19196/19196]

Sepulveda24-picoctf@webshell:~$ ls
challenge.zip
Sepulveda24-picoctf@webshell:~$ unzip challenge.zip 
Archive:  challenge.zip
   creating: drop-in/
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/master  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/ba/
 extracting: drop-in/.git/objects/ba/e247ddd9f730bb7a2a9425d4616b116bc7b07b  
   creating: drop-in/.git/objects/68/
 extracting: drop-in/.git/objects/68/df36301019ecc05a65a4e87a754c83411ac925  
   creating: drop-in/.git/objects/87/
 extracting: drop-in/.git/objects/87/b85d7dfb839b077678611280fa023d76e017b8  
   creating: drop-in/.git/objects/d5/
 extracting: drop-in/.git/objects/d5/52d1ecd2d83fa2e65b6724d1ff73b45a7d59b7  
   creating: drop-in/.git/objects/0c/
 extracting: drop-in/.git/objects/0c/1ab266b7a3a1cd099bb509f82b7a2d03aecd03  
   creating: drop-in/.git/objects/8d/
 extracting: drop-in/.git/objects/8d/c51806c760dfdbb34b33a2008926d3d8e8ad49  
Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/160/challenge.zip
--2025-02-20 21:26:09--  https://artifacts.picoctf.net/c_titan/160/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.18, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17740 (17K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                     100%[===========================================================================================================>]  17.32K  --.-KB/s    in 0s      
Sepulveda24-picoctf@webshell:~$ ssh saturn.picoctf.net -p 49261
The authenticity of host '[saturn.picoctf.net]:49261 ([13.59.203.175]:49261)' can't be established.
ED25519 key fingerprint is SHA256:dMTscRrUiURy7uMu5eGWwEKdd2FzqLzx6LfWhssWnNQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:49261' (ED25519) to the list of known hosts.
Sepulveda24-picoctf@saturn.picoctf.net's password: 
49261
Permission denied, please try again.
Sepulveda24-picoctf@saturn.picoctf.net's password: 
Permission denied, please try again.
Sepulveda24-picoctf@saturn.picoctf.net's password: 
Sepulveda24-picoctf@saturn.picoctf.net: Permission denied (publickey,password).
Sepulveda24-picoctf@webshell:~$ ssh saturn.picoctf.net -p 49261
Sepulveda24-picoctf@saturn.picoctf.net's password: 
Permission denied, please try again.
Sepulveda24-picoctf@saturn.picoctf.net's password: 
Permission denied, please try again.
Sepulveda24-picoctf@saturn.picoctf.net's password: 
Sepulveda24-picoctf@saturn.picoctf.net: Permission denied (publickey,password).
Sepulveda24-picoctf@webshell:~$ ssh saturn.picoctf.net -p 49261
Sepulveda24-picoctf@saturn.picoctf.net's password: 
Permission denied, please try again.
Sepulveda24-picoctf@saturn.picoctf.net's password: 


Permission denied, please try again.
Sepulveda24-picoctf@saturn.picoctf.net's password: 
Sepulveda24-picoctf@saturn.picoctf.net: Permission denied (publickey,password).
Sepulveda24-picoctf@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 49261
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

picoplayer@challenge:~$ cat /etc/cronotab
cat: /etc/cronotab: No such file or directory
picoplayer@challenge:~$ ls
picoplayer@challenge:~$ cat /etc/crontab 
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_9d5cb744}
picoplayer@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
Sepulveda24-picoctf@webshell:~$ 


Notas adicionales

-------------

Referencias

https://webshell.picoctf.org