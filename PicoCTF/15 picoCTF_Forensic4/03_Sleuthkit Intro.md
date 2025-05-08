Descripción
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

Additional details will be available after launching your challenge instance.
Hints:
1.⁠ (none)

Con terminal linux
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Desktop  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ cd Retos  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ ls        
binwalk       capture.pcap.1  Forensic4  picopico.key    tunn3l_v1s10n.bmp
capture.pcap  dolls.jpg       myenv      picopico.key.1  vulture.jpg
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ cd Forensic4 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ mkdir intro                       
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ cd intro    
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/intro]
└─$ 

┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4/intro]
└─$ cd /tmp                  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/tmp]
└─$ ls
mozilla_parallels0
ssh-fitriAv5PPUA
systemd-private-2f8d46286014499abde9a926c5927b2e-colord.service-ZTDs9u
systemd-private-2f8d46286014499abde9a926c5927b2e-haveged.service-aaaaaa
systemd-private-2f8d46286014499abde9a926c5927b2e-ModemManager.service-aaaaaa
systemd-private-2f8d46286014499abde9a926c5927b2e-systemd-logind.service-aaaaaa
systemd-private-2f8d46286014499abde9a926c5927b2e-upower.service-pFOuWl
Temp-dd10fa5d-7c45-4469-8bf0-4e12f5b80044
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/tmp]
└─$ wget Download the disk image and use mmls on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.
Note: if you are using the webshell, download and extract the disk image into /tmp not your home directory.
Download disk image
Additional details will be available after launching your challenge         
--2025-05-08 08:38:59--  http://download/
Resolving download (download)... failed: No address associated with hostname.
wget: unable to resolve host address ‘download’
--2025-05-08 08:38:59--  http://the/
Resolving the (the)... failed: Name or service not known.
wget: unable to resolve host address ‘the’
--2025-05-08 08:38:59--  http://disk/
Resolving disk (disk)... failed: Name or service not known.
wget: unable to resolve host address ‘disk’
--2025-05-08 08:38:59--  http://image/
Resolving image (image)... failed: Name or service not known.
wget: unable to resolve host address ‘image’
--2025-05-08 08:38:59--  http://and/
Resolving and (and)... failed: Name or service not known.
wget: unable to resolve host address ‘and’
--2025-05-08 08:38:59--  http://use/
Resolving use (use)... failed: Name or service not known.
wget: unable to resolve host address ‘use’
--2025-05-08 08:38:59--  http://mmls/
Resolving mmls (mmls)... failed: Name or service not known.
wget: unable to resolve host address ‘mmls’
--2025-05-08 08:38:59--  http://on/
Resolving on (on)... failed: Name or service not known.
wget: unable to resolve host address ‘on’
--2025-05-08 08:38:59--  http://it/
Resolving it (it)... failed: No address associated with hostname.
wget: unable to resolve host address ‘it’
--2025-05-08 08:39:00--  http://to/
Resolving to (to)... failed: No address associated with hostname.
wget: unable to resolve host address ‘to’
--2025-05-08 08:39:00--  http://find/
Resolving find (find)... failed: Name or service not known.
wget: unable to resolve host address ‘find’
--2025-05-08 08:39:10--  http://the/
Resolving the (the)... failed: Name or service not known.
wget: unable to resolve host address ‘the’
--2025-05-08 08:39:10--  http://size/
Resolving size (size)... failed: Name or service not known.
wget: unable to resolve host address ‘size’
--2025-05-08 08:39:10--  http://of/
Resolving of (of)... failed: Name or service not known.
wget: unable to resolve host address ‘of’
--2025-05-08 08:39:10--  http://the/
Resolving the (the)... failed: Name or service not known.
wget: unable to resolve host address ‘the’
--2025-05-08 08:39:10--  http://linux/
Resolving linux (linux)... failed: Name or service not known.
wget: unable to resolve host address ‘linux’
--2025-05-08 08:39:10--  http://partition./
Resolving partition. (partition.)... failed: Name or service not known.
wget: unable to resolve host address ‘partition.’
--2025-05-08 08:39:10--  http://connect/
Resolving connect (connect)... failed: Name or service not known.
wget: unable to resolve host address ‘connect’
--2025-05-08 08:39:11--  http://to/
Resolving to (to)... failed: No address associated with hostname.
wget: unable to resolve host address ‘to’
--2025-05-08 08:39:11--  http://the/
Resolving the (the)... failed: Name or service not known.
wget: unable to resolve host address ‘the’
--2025-05-08 08:39:11--  http://remote/
Resolving remote (remote)... failed: Name or service not known.
wget: unable to resolve host address ‘remote’
--2025-05-08 08:39:11--  http://checker/
Resolving checker (checker)... failed: Name or service not known.
wget: unable to resolve host address ‘checker’
--2025-05-08 08:39:11--  http://service/
Resolving service (service)... failed: Name or service not known.
wget: unable to resolve host address ‘service’
--2025-05-08 08:39:11--  http://to/
Resolving to (to)... failed: No address associated with hostname.
wget: unable to resolve host address ‘to’
--2025-05-08 08:39:11--  http://check/
Resolving check (check)... failed: Name or service not known.
wget: unable to resolve host address ‘check’
--2025-05-08 08:39:11--  http://your/
Resolving your (your)... failed: Name or service not known.
wget: unable to resolve host address ‘your’
--2025-05-08 08:39:11--  http://answer/
Resolving answer (answer)... failed: Name or service not known.
wget: unable to resolve host address ‘answer’
--2025-05-08 08:39:12--  http://and/
Resolving and (and)... failed: Name or service not known.
wget: unable to resolve host address ‘and’
--2025-05-08 08:39:17--  http://get/
Resolving get (get)... failed: Name or service not known.
wget: unable to resolve host address ‘get’
--2025-05-08 08:39:17--  http://the/
Resolving the (the)... failed: Name or service not known.
wget: unable to resolve host address ‘the’
--2025-05-08 08:39:17--  http://flag./
Resolving flag. (flag.)... failed: Name or service not known.
wget: unable to resolve host address ‘flag.’
zsh: command not found: Note:
zsh: command not found: Download
zsh: command not found: Additional
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/tmp]
└─$ wgt https://artifacts.picoctf.net/c/164/disk.img.gz
zsh: command not found: wgt
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/tmp]
└─$ wget https://artifacts.picoctf.net/c/164/disk.img.gz
--2025-05-08 08:39:35--  https://artifacts.picoctf.net/c/164/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.100, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29714372 (28M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz         100%[================>]  28.34M  19.9MB/s    in 1.4s    

2025-05-08 08:39:37 (19.9 MB/s) - ‘disk.img.gz’ saved [29714372/29714372]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/tmp]
└─$ gzip disk.img.gz                                   
gzip: disk.img.gz already has .gz suffix -- unchanged
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/tmp]
└─$ gzip -d disk.img.gz
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/tmp]
└─$ ls
disk.img
mozilla_parallels0
ssh-fitriAv5PPUA
systemd-private-2f8d46286014499abde9a926c5927b2e-colord.service-ZTDs9u
systemd-private-2f8d46286014499abde9a926c5927b2e-haveged.service-aaaaaa
systemd-private-2f8d46286014499abde9a926c5927b2e-ModemManager.service-aaaaaa
systemd-private-2f8d46286014499abde9a926c5927b2e-systemd-logind.service-aaaaaa
systemd-private-2f8d46286014499abde9a926c5927b2e-upower.service-pFOuWl
Temp-dd10fa5d-7c45-4469-8bf0-4e12f5b80044
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/tmp]
└─$ mmls disk.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/tmp]
└─$ nc saturn.picoctf.net 50861
What is the size of the Linux partition in the given disk image?
Length in sectors: 0000202752 
0000202752 
Great work!




picoCTF{mm15_f7w!}




Notas adicionales

--------------------


Referencias

https://artifacts.picoctf.net/c/164/disk.img.gz