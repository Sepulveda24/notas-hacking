Descripción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.

Hints:
1.⁠ ⁠Try using a tool like Wireshark
2.What are streams?

Solución 1

Con wireshark

Se hace una captura de un trafico de red, donde muestra el numero de columnas hora de generacion del paquete, protocolo, etc
Despues se selecciona un paquete udm y se le hace stream para ver la bandera
─(parallels㉿kali-linux-2022-2)-[~]
└─$ wget https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap
--2025-04-02 23:50:24--  https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 239455 (234K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap        100%[================>] 233.84K   805KB/s    in 0.3s    

2025-04-02 23:50:25 (805 KB/s) - ‘capture.pcap’ saved [239455/239455]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 capture.pcap   Downloads    Pictures   '~.venv'
 cookies.txt    flag.png     Public      Videos
 Desktop        garden.jpg   server.py   webshell.php
 Documents      Music        Templates   webshell.png.php
                                                              
picoCTF{Stat31355_636f6e6e}


Notas adicionales

--------------------


Referencias

https://www.solarwinds.com/resources/it-glossary/pcap