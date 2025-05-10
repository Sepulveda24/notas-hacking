Descripción
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/b4d62f6e431dc8e563309ea8c33a06b3/cat.jpg)




Hints:
1.⁠ ⁠Look at the details of the file
2.Make sure to submit the flag as picoCTF{XXXXX}

Solución 1

Con webshell y cyberchef
Sepulveda24-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/b4d62f6e431dc8e563309ea8c33a06b3/cat.jp 
--2025-05-10 15:49:34--  https://mercury.picoctf.net/static/b4d62f6e431dc8e563309ea8c33a06b3/cat.jp
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 404 Not Found
2025-05-10 15:49:34 ERROR 404: Not Found.

Sepulveda24-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/b4d62f6e431dc8e563309ea8c33a06b3/cat.jpg
--2025-05-10 15:49:38--  https://mercury.picoctf.net/static/b4d62f6e431dc8e563309ea8c33a06b3/cat.jpg
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 878136 (858K) [application/octet-stream]
Saving to: 'cat.jpg'

cat.jpg                                           100%[===========================================================================================================>] 857.55K  1.86MB/s    in 0.5s    

2025-05-10 15:49:38 (1.86 MB/s) - 'cat.jpg' saved [878136/878136]

Sepulveda24-picoctf@webshell:~$ ls
README.txt  capture.pcap  cat.jpg  picopico.key  ukn_reality.jpg  unknown.zip
Sepulveda24-picoctf@webshell:~$ exiftool ca
capture.pcap  cat.jpg       
Sepulveda24-picoctf@webshell:~$ exiftool ca
capture.pcap  cat.jpg       
Sepulveda24-picoctf@webshell:~$ exiftool cat.jpg 
ExifTool Version Number         : 12.40
File Name                       : cat.jpg
Directory                       : .
File Size                       : 858 KiB
File Modification Date/Time     : 2021:03:15 18:24:46+00:00
File Access Date/Time           : 2025:05:10 15:49:38+00:00
File Inode Change Date/Time     : 2025:05:10 15:49:38+00:00
File Permissions                : -rw-rw-r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
Sepulveda24-picoctf@webshell:~$ 


cyberchef 
input:cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Recipe:from 64
output:picoCTF{the_m3tadata_1s_modified}


Notas adicionales

--------------------


Referencias

https://webshell.picoctf.org
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnQwYUdWZmJUTjBZV1JoZEdGZk1YTmZiVzlrYVdacFpXUjk