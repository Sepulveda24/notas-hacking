Descripción
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/138/disk.flag.img.gz)

Hints:
1.⁠ ⁠(none)

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
└─$ cd Forensic4 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ ls
concat_v.png  dds1-alpine.flag.img  intro
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ cd introA   
cd: no such file or directory: introA
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ mkdir introA 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ cd introA 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ wget https://artifacts.picoctf.net/c/138/disk.flag.img.gz
--2025-05-08 08:46:55--  https://artifacts.picoctf.net/c/138/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.26, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 47534528 (45M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz    100%[================>]  45.33M  23.6MB/s    in 1.9s    

2025-05-08 08:46:57 (23.6 MB/s) - ‘disk.flag.img.gz’ saved [47534528/47534528]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ gzip -d disk.flag.img.gz 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ ls
disk.flag.img
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ mmls disk.flag.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ fls disk.flag.img -o 0000360448             
d/d 451:        home
d/d 11: lost+found
d/d 12: boot
d/d 1985:       etc
d/d 1986:       proc
d/d 1987:       dev
d/d 1988:       tmp
d/d 1989:       lib
d/d 1990:       var
d/d 3969:       usr
d/d 3970:       bin
d/d 1991:       sbin
d/d 1992:       media
d/d 1993:       mnt
d/d 1994:       opt
d/d 1995:       root
d/d 1996:       run
d/d 1997:       srv
d/d 1998:       sys
d/d 2358:       swap
V/V 31745:      $OrphanFiles
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ -r
zsh: command not found: -r
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ fls disk.flag.img -o 0000360448 -r
d/d 451:        home
d/d 11: lost+found
d/d 12: boot
d/d 1985:       etc
+ r/r 23:       group
+ r/r 24:       group-
+ r/r 25:       shadow
+ r/r 26:       shadow-
+ r/r 27:       passwd
+ r/r 28:       passwd-
+ r/r 29:       hosts
+ d/d 30:       zoneinfo

┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ fls disk.flag.img -o 0000360448 -r | grep pico
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ fls disk.flag.img -o 0000360448 -r | grep flag
++ r/r * 2082(realloc): flag.txt
++ r/r 2371:    flag.uni.txt
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ fls disk.flag.img -o 0000360448 -r | 2371     
zsh: command not found: 2371
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ fls disk.flag.img -o 0000360448 -r 2371  
Error extracting file from image (ext2fs_dir_open_meta: Error reading directory contents: 2371
)
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ icat disk.flag.img -o 0000360448 -r 2371
picoCTF{by73_5urf3r_2f22df38}
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/introA]
└─$ 




picoCTF{by73_5urf3r_2f22df38}



Notas adicionales

--------------------


Referencias

terminal linux