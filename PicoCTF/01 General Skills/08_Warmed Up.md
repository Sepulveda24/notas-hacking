Descripción
What is 0x3D (base 16) in decimal (base 10)?

Hints:
1.Submit your answer in our flag format. For example, if your answer was '22', you would submit 'picoCTF{22}' as the flag.


Solución 1 
Con Python

Sepulveda24-picoctf@webshell:~$ python
Python 3.10.12 (main, Sep 11 2024, 22:47:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> numero = 0x3D 
>>> numero_decimal = int(numero)
>>> print (numero_decimal)
61


Solucion 2

Usando cyberchef https://gchq.github.io/CyberChef/#recipe=From_Base(16)To_Base(10)&input=MHgzRCAK&oenc=65001


'''
Input: 0x3D 
Recipe: from base  16
to base 10
Output: 61
'''

Notas adicionales

Referencias

https://gchq.github.io/CyberChef/#recipe=From_Base(16)To_Base(10)&input=MHgzRCAK&oenc=65001
https://webshell.picoctf.org