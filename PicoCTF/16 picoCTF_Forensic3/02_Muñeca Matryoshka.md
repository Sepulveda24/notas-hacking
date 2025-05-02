Descripción
Las muñecas Matryoshka son un conjunto de muñecas de madera de tamaño decreciente colocadas una dentro de otra. ¿Cuál es el último? Imagen: [este](https://mercury.picoctf.net/static/5eb456e480e485183c9c1b16952c6eda/dolls.jpg)


Hints:
1.⁠ ⁠Espera, ¿puedes ocultar archivos dentro de archivos? ¿Pero cómo los encuentras?
2.Asegúrese de enviar la bandera como picoCTF{XXXXX}

Solución 1

Con Webshell
Sepulveda24-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/5eb456e480e485183c9c1b16952c6eda/dolls.jpg
--2025-05-02 21:14:02--  https://mercury.picoctf.net/static/5eb456e480e485183c9c1b16952c6eda/dolls.jpg
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 651636 (636K) [application/octet-stream]
Saving to: 'dolls.jpg'

dolls.jpg                                         100%[===========================================================================================================>] 636.36K  1.87MB/s    in 0.3s    

2025-05-02 21:14:02 (1.87 MB/s) - 'dolls.jpg' saved [651636/651636]

Sepulveda24-picoctf@webshell:~$ ls
'Forensics is fun.pptm'   README.txt  '[Content_Types].xml'   _rels   docProps   dolls.jpg   index.html   ppt
Sepulveda24-picoctf@webshell:~$ binwalk dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378956, uncompressed size: 383938, name: base_images/2_c.jpg
651614        0x9F15E         End of Zip archive, footer length: 22

Sepulveda24-picoctf@webshell:~$ ls
'Forensics is fun.pptm'   README.txt  '[Content_Types].xml'   _rels   docProps   dolls.jpg   index.html   ppt
Sepulveda24-picoctf@webshell:~$ binwalk -e  dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378956, uncompressed size: 383938, name: base_images/2_c.jpg
651614        0x9F15E         End of Zip archive, footer length: 22

Sepulveda24-picoctf@webshell:~$ ls
'Forensics is fun.pptm'   README.txt  '[Content_Types].xml'   _dolls.jpg.extracted   _rels   docProps   dolls.jpg   index.html   ppt
Sepulveda24-picoctf@webshell:~$ cd _dolls.jpg.extracted/
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted$ ls
4286C.zip  base_images
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted$ cd base_images/
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images$ ls
2_c.jpg
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images$ binwalk 2_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196043, uncompressed size: 201445, name: base_images/3_c.jpg
383805        0x5DB3D         End of Zip archive, footer length: 22
383916        0x5DBAC         End of Zip archive, footer length: 22

Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images$ binwalk -e 2_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196043, uncompressed size: 201445, name: base_images/3_c.jpg
383805        0x5DB3D         End of Zip archive, footer length: 22
383916        0x5DBAC         End of Zip archive, footer length: 22

Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images$ ls
2_c.jpg  _2_c.jpg.extracted
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images$ cd _2_c.jpg.extracted/
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted$ ls
2DD3B.zip  base_images
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted$ cd base_images/
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ ls
3_c.jpg
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ binwalk -e 3_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77651, uncompressed size: 79808, name: base_images/4_c.jpg
201423        0x312CF         End of Zip archive, footer length: 22

Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ ls
3_c.jpg  _3_c.jpg.extracted
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ cd _3_c.jpg.extracted/
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted$ ls
1E2D6.zip  base_images
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted$ cd base_images/
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ ls
4_c.jpg
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ binwalk -e 4_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 64, uncompressed size: 81, name: flag.txt
79786         0x137AA         End of Zip archive, footer length: 22

Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ ls
4_c.jpg  _4_c.jpg.extracted
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ cd _4_c.jpg.extracted/
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ ls
136DA.zip  flag.txt
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ open flag.txt 
"/home/Sepulveda24-picoctf/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted/flag.txt" may be a binary file.  See it anyway? 
Warning: program returned non-zero exit code #256
Sepulveda24-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ 
picoCTF{336cf6d51c9d9774fd37196c1d7320ff}
Notas adicionales

--------------------


Referencias

https://webshell.picoctf.org