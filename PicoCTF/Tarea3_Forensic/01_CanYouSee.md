Descripción
How about some hide and seek?Download this file [here](https://artifacts.picoctf.net/c_titan/131/unknown.zip).



Hints:
1.⁠ ⁠How can you view the information about the picture?
2.If something isn't in the expected form, maybe it deserves attention?

Solución 1

Con webshel y cyberchef
Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/131/unknown.zip
--2025-05-10 15:39:59--  https://artifacts.picoctf.net/c_titan/131/unknown.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2252296 (2.1M) [application/octet-stream]
Saving to: 'unknown.zip'

unknown.zip                                       100%[===========================================================================================================>]   2.15M  1.83MB/s    in 1.2s    

2025-05-10 15:40:00 (1.83 MB/s) - 'unknown.zip' saved [2252296/2252296]

Sepulveda24-picoctf@webshell:~$ ls
README.txt  capture.pcap  picopico.key  unknown.zip
Sepulveda24-picoctf@webshell:~$ file unknown.zip 
unknown.zip: Zip archive data, at least v2.0 to extract, compression method=deflate
Sepulveda24-picoctf@webshell:~$ unzip unknown.zip 
Archive:  unknown.zip
  inflating: ukn_reality.jpg         
Sepulveda24-picoctf@webshell:~$ ls
README.txt  capture.pcap  picopico.key  ukn_reality.jpg  unknown.zip
Sepulveda24-picoctf@webshell:~$ exittools ukn_reality.jpg 
-bash: exittools: command not found
Sepulveda24-picoctf@webshell:~$ exitools ukn_reality.jpg 
-bash: exitools: command not found
Sepulveda24-picoctf@webshell:~$ exifools ukn_reality.jpg 
-bash: exifools: command not found
Sepulveda24-picoctf@webshell:~$ exiftools ukn_reality.jpg 
-bash: exiftools: command not found
Sepulveda24-picoctf@webshell:~$ exiftool ukn_reality.jpg 
ExifTool Version Number         : 12.40
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.2 MiB
File Modification Date/Time     : 2024:03:12 00:05:57+00:00
File Access Date/Time           : 2024:03:12 00:05:57+00:00
File Inode Change Date/Time     : 2025:05:10 15:41:29+00:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fZDhjMzgxZmR9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
Sepulveda24-picoctf@webshell:~$ 


cyberchef 
input:cGljb0NURntNRTc0RDQ3QV9ISUREM05fZDhjMzgxZmR9Cg==
Recipe:from 64
output:picoCTF{ME74D47A_HIDD3N_d8c381fd}








Notas adicionales

--------------------


Referencias

https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnROUlRjMFJEUTNRVjlJU1VSRU0wNWZaRGhqTXpneFptUjlDZz09

https://webshell.picoctf.org