Descripción
Ejecute el script de Python y convierta el número dado de decimal a binario para obtener la bandera.[Descargar script de Python](https://artifacts.picoctf.net/c/24/convertme.py)

Hints:
1.⁠ ⁠¡Busque una aplicación de conversión de números decimales a binarios en la web o use la calculadora de su computadora!
2.The `str_xor` function does not need to be reverse engineered for this challenge.
3.If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget`command in the webshell.
4.To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
5Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
6.Finalmente, para ejecutar el script, escriba todo después del signo de dólar y luego presione enter:`$ python3 convertme.py`

Solución 1

Con web shell y cyberchef


Sepulveda24-picoctf@webshell:~$ ls
README.txt  code.py  codebook.txt  enc_flag  strings
Sepulveda24-picoctf@webshell:~$ rm -ff *
Sepulveda24-picoctf@webshell:~$ ls
Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2025-02-20 17:48:07--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.42, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                                      100%[===========================================================================================================>]   1.16K  --.-KB/s    in 0s      

2025-02-20 17:48:07 (303 MB/s) - 'convertme.py' saved [1189/1189]

Sepulveda24-picoctf@webshell:~$ ls
convertme.py
Sepulveda24-picoctf@webshell:~$ python covertme.py
python: can't open file '/home/Sepulveda24-picoctf/covertme.py': [Errno 2] No such file or directory
Sepulveda24-picoctf@webshell:~$ python convertme.py 
If 52 is in decimal base, what is it in binary base?
Answer: 00110100
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
Sepulveda24-picoctf@webshell:~$ 


Usando cyberchef https://gchq.github.io/CyberChef/#recipe=From_Decimal('Space',false)To_Binary('Space',8)&input=NTI&oeol=FF

'''
Input: 52
Recipe: from decimal  
to binary
Output: 00110100
'''




Notas adicionales

-------------

Referencias

https://webshell.picoctf.org
https://gchq.github.io/CyberChef/#recipe=From_Decimal('Space',false)To_Binary('Space',8)&input=NTI&oeol=FF
