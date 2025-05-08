Descripción
Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

Additional details will be available after launching your challenge instance.


Hints:
1.⁠ ⁠(none)

Solución 1

Con terminal linux

                                                                             ┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Desktop        
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ cd Retos  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ cd Forensic4 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ mkdir operation_oni  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ wget https://artifacts.picoctf.net/c/71/disk.img.gz      
--2025-05-08 13:10:55--  https://artifacts.picoctf.net/c/71/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.64, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 48132743 (46M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz         100%[================>]  45.90M  19.5MB/s    in 2.4s    

2025-05-08 13:10:58 (19.5 MB/s) - ‘disk.img.gz’ saved [48132743/48132743]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ gzip -d disk.img.gz                         
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ mmls disk.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ fls disk.img -o 206848                                                  
d/d 458:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 79: proc
d/d 80: dev
d/d 81: tmp
d/d 82: lib
d/d 85: var
d/d 94: usr
d/d 104:        bin
d/d 118:        sbin
d/d 464:        media
d/d 468:        mnt
d/d 469:        opt
d/d 470:        root
d/d 471:        run
d/d 473:        srv
d/d 474:        sys
V/V 33049:      $OrphanFiles
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ fls disk.img -o 206848 470
r/r 2344:       .ash_history
d/d 3916:       .ssh
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ fls disk.img -o 206848 3916
r/r 2345:       id_ed25519
r/r 2346:       id_ed25519.pub
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ fls disk.img -o 206848 2345 >key_file
Error extracting file from image (ext2fs_dir_open_meta: Error reading directory contents: 2345
)
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ icat disk.img -o 206848 2345 >key_file
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ file key_file                        
key_file: OpenSSH private key
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ chmod 600 key_file                    
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ ssh -i key_file -p 58715 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:58715 ([13.59.203.175]:58715)' can't be established.
ED25519 key fingerprint is SHA256:XBSvB1lk28EctsAVdKJtsl0A7C5bonqPrvHCYH8aEy4.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:58715' (ED25519) to the list of known hosts.
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

ctf-player@challenge:~$ cat flag.txt 
picoCTF{k3y_5l3u7h_af277f77}ctf-player@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
                                       

picoCTF{k3y_5l3u7h_af277f77}


Notas adicionales

--------------------


Referencias

terminal linux