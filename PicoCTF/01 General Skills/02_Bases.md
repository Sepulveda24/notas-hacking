Descripción
What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.
Hints:
1.⁠ ⁠Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

Solución
Con Python

Sepulveda24-picoctf@webshell:~$ python
Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import base64
>>> codigo = "bDNhcm5fdGgzX3IwcDM1"
>>> decodificar_bytes = base64.b64decode(codigo)
>>> decodificar= decodificar_bytes.decode("utf-8")
>>> print(decodificar)
l3arn_th3_r0p35
>>> 






Solución 2
Usando cyberchef https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YkROaGNtNWZkR2d6WDNJd2NETTE

'''
Input: bDNhcm5fdGgzX3IwcDM1
Recipe: from base  64
Output: l3arn_th3_r0p35
'''

Notas adicionales

Referencias
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YkROaGNtNWZkR2d6WDNJd2NETTE


https://docs.python.org/es/3.10/library/json.html