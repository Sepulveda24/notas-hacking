Descripción
Find the flag in this picture.

Hints:
1.⁠ ⁠(none)

Solución 1

Con webshell-exiftool

wget Sepulveda24-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/00efdf2961da1e21470ffc0d496c3cc2/pico_img.png
--2025-04-03 06:04:57--  https://jupiter.challenges.picoctf.org/static/00efdf2961da1e21470ffc0d496c3cc2/pico_img.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108795 (106K) [application/octet-stream]
Saving to: 'pico_img.png.1'

pico_img.png.1                                    100%[===========================================================================================================>] 106.25K  --.-KB/s    in 0.05s   

2025-04-03 06:04:57 (2.17 MB/s) - 'pico_img.png.1' saved [108795/108795]

Sepulveda24-picoctf@webshell:~$ ls
README.txt  challenge.zip  cookies.txt  drop-in  flag  flag.1  flag.2  flag.png  pico_img.png  pico_img.png.1  server.py  server.py.1
Sepulveda24-picoctf@webshell:~$ exiftool pico_img.png
ExifTool Version Number         : 12.40
File Name                       : pico_img.png
Directory                       : .
File Size                       : 106 KiB
File Modification Date/Time     : 2020:10:26 18:38:23+00:00
File Access Date/Time           : 2025:04:03 06:04:52+00:00
File Inode Change Date/Time     : 2025:04:03 06:04:52+00:00
File Permissions                : -rw-rw-r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 600
Image Height                    : 600
Bit Depth                       : 8
Color Type                      : RGB
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Software                        : Adobe ImageReady
XMP Toolkit                     : Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27
Creator Tool                    : Adobe Photoshop CS6 (Windows)
Instance ID                     : xmp.iid:A5566E73B2B811E8BC7F9A4303DF1F9B
Document ID                     : xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B
Derived From Instance ID        : xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B
Derived From Document ID        : xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B
Warning                         : [minor] Text/EXIF chunk(s) found after PNG IDAT (may be ignored by some readers)
Artist                          : picoCTF{s0_m3ta_fec06741}
Image Size                      : 600x600
Megapixels                      : 0.360
Sepulveda24-picoctf@webshell:~$ 


picoCTF{s0_m3ta_fec06741}


Notas adicionales

--------------------


Referencias

https://www.geoidep.gob.pe/catalogo-metadatos/que-son-los-metadatos#:~:text=La%20definición%20más%20concreta%20de,otras%20características%20de%20los%20datos.

https://webshell.picoctf.org