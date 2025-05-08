Descripción
Encontramos esta [captura de paquete](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) y [clave](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recupera la bandera.


Hints:
1.⁠ ⁠Prueba a usar una herramienta como Wireshark.
2.¿Cómo se puede descifrar el flujo TLS?

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
└─$ ls
binwalk  dolls.jpg  myenv  tunn3l_v1s10n.bmp
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap
--2025-05-02 16:04:56--  https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 13163 (13K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap        100%[================>]  12.85K  --.-KB/s    in 0s      

2025-05-02 16:05:01 (113 MB/s) - ‘capture.pcap’ saved [13163/13163]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key     
zsh: no such file or directory: https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key
--2025-05-02 16:05:13--  https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key’

picopico.key        100%[================>]   1.66K  --.-KB/s    in 0.002s  

2025-05-02 16:05:19 (740 KB/s) - ‘picopico.key’ saved [1704/1704]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ ls
binwalk  capture.pcap  dolls.jpg  myenv  picopico.key  tunn3l_v1s10n.bmp
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ wireshark capture.pcap 
libGL error: pci id for fd 19: 1ab8:0010, driver (null)
pci id for fd 20: 1ab8:0010, driver (null)
 ** (wireshark:48436) 16:09:17.621044 [GUI WARNING] -- FIX Add drag reordering to UAT dialog



picoCTF{nongshim.shrimp.crackers} 

Notas adicionales

--------------------


Referencias

https://github.com/payloadbox/xxe-injection-payload-list

