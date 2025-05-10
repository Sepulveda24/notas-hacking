Descripción
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/2/challenge.zip)

Additional details will be available after launching your challenge instance.



Hints:
1.⁠ ⁠QR codes are a way of encoding data. While they're most known for storing URLs, they can store other things too.
2.Mobile phones have included native QR code scanners in their cameras since version 8 (Oreo) and iOS 11
3.If you don't have access to a phone, you can also use zbar-tools to convert an image to text

Solución 1

Con Webshell
📚  For more information and a beginner's guide, type less ~/README.txt.
Sepulveda24-picoctf@webshell:~$ ssh -p 60050 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:60050 ([18.217.83.136]:60050)' can't be established.
ED25519 key fingerprint is SHA256:hVmbk/OaNT4902bBr7h26wfhmBuJWi4tub8AJqoAJCM.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:60050' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
                                                                  
ctf-player@challenge:~/drop-in$ ls
flag.png
ctf-player@challenge:~/drop-in$ zbarimg flag.png 
Connection Error (Failed to connect to socket /var/run/dbus/system_bus_socket: No such file or directory)
Connection Null
QR-Code:picoCTF{p33k_@_b00_b5ce2572}
scanned 1 barcode symbols from 1 images in 0 seconds

ctf-player@challenge:~/drop-in$ Connection to atlas.picoctf.net closed by remote host.
Connection to atlas.picoctf.net closed.
Sepulveda24-picoctf@webshell:~$ 



picoCTF{p33k_@_b00_b5ce2572}



Notas adicionales

--------------------


Referencias

https://webshell.picoctf.org