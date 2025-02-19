Descripción
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip)

Hints:
1.⁠ ⁠After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...


Solución 1

Con web shell


Sepulveda24-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip
--2025-02-18 18:43:18--  https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4520 (4.4K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip'

Addadshashanammu.zip                              100%[===========================================================================================================>]   4.41K  --.-KB/s    in 0s      

2025-02-18 18:43:18 (3.16 GB/s) - 'Addadshashanammu.zip' saved [4520/4520]

Sepulveda24-picoctf@webshell:~$ ls
Addadshashanammu.zip  README.txt
Sepulveda24-picoctf@webshell:~$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
Sepulveda24-picoctf@webshell:~$ ls
Addadshashanammu  Addadshashanammu.zip  README.txt
Sepulveda24-picoctf@webshell:~$ cd Addadshashanammu/
Sepulveda24-picoctf@webshell:~/Addadshashanammu$ ls
Almurbalarammi
Sepulveda24-picoctf@webshell:~/Addadshashanammu$ cd Almurbalarammi/
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi$ ls
Ashalmimilkala
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi$ cd Ashalmimilkala/
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala$ ls
Assurnabitashpi
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala$ cd Assurnabitashpi/
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi$ ls
Maelkashishi
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi$ cd Maelkashishi/
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi$ ls
Onnissiralis
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi$ cd Onnissiralis/
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ ls
Ularradallaku
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ cd Ularradallaku/
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ file fang-of-haynekhtnamet 
fang-of-haynekhtnamet: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=fcea24fb5379795a123bb860267d815e889a6d23, not stripped
Sepulveda24-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_d32e018c}



Notas adicionales

--------------
Referencias


https://webshell.picoctf.org