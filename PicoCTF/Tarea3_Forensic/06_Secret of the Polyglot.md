Descripción
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/8/flag2of2-final.pdf).


Hints:
1.⁠ This problem can be solved by just opening the file in different ways

Solución 1

Con terminal linux
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Desktop        
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ ls
 firefox-esr  'Parallels Shared Folders'   Retos
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ cd Retos  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ mkdir TareaForensic3
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ cd TareaForensic3 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3]
└─$ ls
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3]
└─$ mkdir secretOfThePolyglot
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3]
└─$ cd secretOfThePolyglot 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/secretOfThePolyglot]
└─$ wget https://artifacts.picoctf.net/c_titan/8/flag2of2-final.pdf
--2025-05-10 11:55:55--  https://artifacts.picoctf.net/c_titan/8/flag2of2-final.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.100, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3362 (3.3K) [application/octet-stream]
Saving to: ‘flag2of2-final.pdf’

flag2of2-final.pdf  100%[================>]   3.28K  --.-KB/s    in 0s      

2025-05-10 11:56:00 (39.3 MB/s) - ‘flag2of2-final.pdf’ saved [3362/3362]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/secretOfThePolyglot]
└─$ ls
flag2of2-final.pdf
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/secretOfThePolyglot]
└─$ open flag2of2-final.pdf 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/secretOfThePolyglot]
└─$ cp flag2of2-final.pdf flag2of2-final.png 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/secretOfThePolyglot]
└─$ eog flag2of2-final.png 
zsh: command not found: eog
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/secretOfThePolyglot]
└─$ pip install eog      
error: externally-managed-environment

× This environment is externally managed
╰─> To install Python packages system-wide, try apt install
    python3-xyz, where xyz is the package you are trying to
    install.
    
    If you wish to install a non-Debian-packaged Python package,
    create a virtual environment using python3 -m venv path/to/venv.
    Then use path/to/venv/bin/python and path/to/venv/bin/pip. Make
    sure you have python3-full installed.
    
    If you wish to install a non-Debian packaged Python application,
    it may be easiest to use pipx install xyz, which will manage a
    virtual environment for you. Make sure you have pipx installed.
    
    See /usr/share/doc/python3.13/README.venv for more information.

note: If you believe this is a mistake, please contact your Python installation or OS distribution provider. You can override this, at the risk of breaking your Python installation or OS, by passing --break-system-packages.
hint: See PEP 668 for the detailed specification.
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/secretOfThePolyglot]
└─$ sudo install eog                                      
[sudo] password for parallels: 
install: missing destination file operand after 'eog'
Try 'install --help' for more information.
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/secretOfThePolyglot]
└─$ open flag2of2-final.png 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/secretOfThePolyglot]
└─$ open flag2of2-final.pdf 


picoCTF{f1u3n7_1n_pn9_&_pdf_249d05c0}


Notas adicionales

--------------------


Referencias

Terminal linux