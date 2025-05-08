Descripción
Nos da un enlace en forma de vaso de leche

Hints:
1.⁠ ⁠Look at the problem category

Solución 1

Con terminal linux

                                                                             ┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 binwalk-env            fixme1.tar.gz            Music       Templates
'[Content_Types].xml'   fixme2                   Pictures   '~.venv'
 Desktop                fixme2.tar.gz            ppt         Videos
 docProps               fixme3                   Public
 Documents              fixme3.tar.gz            _rels
 Downloads             'Forensics is fun.pptm'   shell.php
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Desktop 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ ls
 firefox-esr  'Parallels Shared Folders'   Retos
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ cd Retos  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ mkdir Forensic4                   
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ cd Forensic4 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ ls
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ wget http://mercury.picoctf.net:58537/concat_v.png
--2025-05-08 08:08:15--  http://mercury.picoctf.net:58537/concat_v.png
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:58537... connected.
HTTP request sent, awaiting response... 200 OK
Length: 18095920 (17M) [image/png]
Saving to: ‘concat_v.png’

concat_v.png        100%[================>]  17.26M  5.12MB/s    in 3.4s    

2025-05-08 08:08:19 (5.12 MB/s) - ‘concat_v.png’ saved [18095920/18095920]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ sudo apt intall zsteg             
[sudo] password for parallels: 
E: Invalid operation intall
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ sudo apt install zsteg
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
E: Unable to locate package zsteg
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ gm                                                 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ gem install zsteg
Fetching zsteg-0.2.13.gem
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /var/lib/gems/3.0.0 directory.
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ sudo gem install zsteg
Successfully installed zsteg-0.2.13
Parsing documentation for zsteg-0.2.13
Done installing documentation for zsteg after 0 seconds
1 gem installed
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ zsteg -h                                     
Usage: zsteg [options] filename.png [param_string]

    -a, --all                        try all known methods
    -E, --extract NAME               extract specified payload, NAME is like '1b,rgb,lsb'

Iteration/extraction params:
    -o, --order X                    pixel iteration order (default: 'auto')
                                     valid values: ALL,xy,yx,XY,YX,xY,Xy,bY,...
    -c, --channels X                 channels (R/G/B/A) or any combination, comma separated
                                     valid values: r,g,b,a,rg,bgr,rgba,r3g2b3,...
    -b, --bits N                     number of bits, single int value or '1,3,5' or range '1-8'
                                     advanced: specify individual bits like '00001110' or '0x88'
        --lsb                        least significant bit comes first
        --msb                        most significant bit comes first
    -P, --prime                      analyze/extract only prime bytes/pixels
        --shift N                    prepend N zero bits
        --invert                     invert bits (XOR 0xff)
        --pixel-align                pixel-align hidden data

Analysis params:
    -l, --limit N                    limit bytes checked, 0 = no limit (default: 256)

        --[no-]file                  use 'file' command to detect data type (default: YES)
        --no-strings                 disable ASCII strings finding (default: enabled)
    -s, --strings X                  ASCII strings find mode: first, all, longest, none
                                     (default: first)
    -n, --min-str-len X              minimum string length (default: 8)

    -v, --verbose                    Run verbosely (can be used multiple times)
    -q, --quiet                      Silent any warnings (can be used multiple times)
    -C, --[no-]color                 Force (or disable) color output (default: auto)

PARAMS SHORTCUT
        zsteg fname.png 2b,b,lsb,xy  ==>  --bits 2 --channel b --lsb --order xy
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ zsteg concat_v.png 

picoCTF{imag3_m4n1pul4t10n_sl4p5}


Notas adicionales

--------------------


Referencias

http://mercury.picoctf.net:58537/