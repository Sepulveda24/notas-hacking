Descripción
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?

Hints:
1.⁠ ⁠There is data encoded somewhere... there might be an online decoder.

Solución 1

Con terminal de linux

┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ wget https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png
--2025-04-03 00:10:23--  https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 625219 (611K) [application/octet-stream]
Saving to: ‘buildings.png’

buildings.png       100%[================>] 610.57K  1.54MB/s    in 0.4s    

2025-04-03 00:10:24 (1.54 MB/s) - ‘buildings.png’ saved [625219/625219]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 buildings.png   Documents    Music            Public      Videos
 capture.pcap    Downloads    pico_img.png     server.py   webshell.php
 cookies.txt     flag.png     pico_img.png.1   Templates   webshell.png.php
 Desktop         garden.jpg   Pictures        '~.venv'
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ sudo gem install zsteg       
Fetching rainbow-3.1.1.gem
Fetching zsteg-0.2.13.gem
Fetching zpng-0.4.5.gem
Fetching iostruct-0.5.0.gem
Successfully installed rainbow-3.1.1
Successfully installed zpng-0.4.5
Successfully installed iostruct-0.5.0
Successfully installed zsteg-0.2.13
Parsing documentation for rainbow-3.1.1
Installing ri documentation for rainbow-3.1.1
Parsing documentation for zpng-0.4.5
Installing ri documentation for zpng-0.4.5
Parsing documentation for iostruct-0.5.0
Installing ri documentation for iostruct-0.5.0
Parsing documentation for zsteg-0.2.13
Installing ri documentation for zsteg-0.2.13
Done installing documentation for rainbow, zpng, iostruct, zsteg after 0 seconds
4 gems installed
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ zsteg -a buildings.png | grep pico
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"



picoCTF{h1d1ng_1n_th3_b1t5}"
Notas adicionales

--------------------


Referencias

https://www.kaspersky.com/resource-center/definitions/what-is-steganography#:~:text=Steganography%20is%20the%20practice%20of,then%20extracted%20at%20its%20destination.