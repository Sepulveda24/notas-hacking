Descripción
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/260/flag.png).
Hints:
1.⁠ ⁠(None)
Solución 1

Con webshell
Sepulveda24-picoctf@webshell:~$ ls
README.txt  capture.pcap  cat.jpg  flag.png  flag2of2-final.pdf  picopico.key  red.png  ukn_reality.jpg  unknown.zip
Sepulveda24-picoctf@webshell:~$ sz flag.png 
Sepulveda24-picoctf@webshell:~$ binwalk -e flag.png 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2944, uncompressed size: 3095, name: secret/flag.png
42983         0xA7E7          End of Zip archive, footer length: 22

Sepulveda24-picoctf@webshell:~$ ls
README.txt  _flag.png.extracted  capture.pcap  cat.jpg  flag.png  flag2of2-final.pdf  picopico.key  red.png  ukn_reality.jpg  unknown.zip
Sepulveda24-picoctf@webshell:~$ cd _flag.png.extracted/
Sepulveda24-picoctf@webshell:~/_flag.png.extracted$ ls
29  29.zlib  9B3B.zip  secret
Sepulveda24-picoctf@webshell:~/_flag.png.extracted$ cd secret/
Sepulveda24-picoctf@webshell:~/_flag.png.extracted/secret$ ls
flag.png
Sepulveda24-picoctf@webshell:~/_flag.png.extracted/secret$ sz flag.png 
Sepulveda24-picoctf@webshell:~/_flag.png.extracted/secret$ 




picoCTF{Hiddinng_An_imag3_within_@n_ima9e_ad9f6587}
Notas adicionales

--------------------


Referencias

https://github.com/payloadbox/xxe-injection-payload-list