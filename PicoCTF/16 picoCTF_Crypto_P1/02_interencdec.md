Descripción
Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/111/enc_flag).

Hints:
1.⁠ Engaging in various decoding processes is of utmost importance

Solución 1

Con cyberchef y terminal

┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1/interencdec]
└─$ wget https://artifacts.picoctf.net/c_titan/111/enc_flag        
--2025-05-13 13:08:36--  https://artifacts.picoctf.net/c_titan/111/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.26, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 73 [application/octet-stream]
Saving to: ‘enc_flag’

enc_flag            100%[================>]      73  --.-KB/s    in 0s      

2025-05-13 13:08:36 (79.6 MB/s) - ‘enc_flag’ saved [73/73]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1/interencdec]
└─$ ls
enc_flag
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1/interencdec]
└─$ cat enc_flag                             
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6ZzVNR3N5TXpjNWZRPT0nCg==
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1/interencdec]
└─$ cat enc_flag | base64 -d
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg5MGsyMzc5fQ=='
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1/interencdec]
└─$ echo d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg5MGsyMzc5fQ==|base64 -d
wpjvJAM{jhlzhy_k3jy9wa3k_890k2379}                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1/interencdec]
└─$ 

cyberchef 
'''
Input: wpjvJAM{jhlzhy_k3jy9wa3k_890k2379} 
Recipe: rot13. 19
Output: picoCTF{caesar_d3cr9pt3d_890d2379} 
'''

picoCTF{caesar_d3cr9pt3d_890d2379} 



Notas adicionales

--------------------


Referencias

https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,19)&input=d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg5MGsyMzc5fSA

terminal linux