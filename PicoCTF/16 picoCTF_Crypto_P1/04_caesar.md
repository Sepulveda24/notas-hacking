Descripción
Decrypt this [message](https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext).

Hints:
1.⁠ ⁠caesar cipher [tutorial](https://learncryptography.com/classical-encryption/caesar-cipher)

Solución 1

Con terminal linux y cyberchef

┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1/TheNumber]
└─$ mkdir caesar   
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1/TheNumber]
└─$ cd caesar 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/…/Retos/Actividad_16_cripto1/TheNumber/caesar]
└─$ wget https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext     
--2025-05-13 13:32:31--  https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 35 [application/octet-stream]
Saving to: ‘ciphertext’

ciphertext          100%[================>]      35  --.-KB/s    in 0s      

2025-05-13 13:32:32 (30.8 MB/s) - ‘ciphertext’ saved [35/35]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/…/Retos/Actividad_16_cripto1/TheNumber/caesar]
└─$ ls
ciphertext
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/…/Retos/Actividad_16_cripto1/TheNumber/caesar]
└─$ cat ciphertext          
picoCTF{ynkooejcpdanqxeykjrbdofgkq}  


cyberchef 
'''
Input: ynkooejcpdanqxeykjrbdofgkq
Recipe: rot13. 19
Output: crossingtherubiconvfhsjkou
'''



picoCTF{crossingtherubiconvfhsjkou}


Notas adicionales

--------------------


Referencias

https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,30)&input=eW5rb29lamNwZGFucXhleWtqcmJkb2Zna3E