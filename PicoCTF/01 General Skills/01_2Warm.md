Descripción
Can you convert the number 42 (base 10) to binary (base 2)?

Hints:
1.⁠ ⁠Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

Solución 1

Con Python

Sepulveda24-picoctf@webshell:~$ python
Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> bin(42)
'0b101010'
>>> 
picoCTF{101010}




Solución 2
Usando cyberchef https://gchq.github.io/CyberChef/#recipe=From_Base(10)To_Base(2)&input=NDI

'''
Input: 42
Recipe: from base  10
to base 2
Output: 101010
'''


Solucion 3
Sepulveda24-picoctf@webshell:~$ python
Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> bin(42)[2:]
'101010'

Notas adicionales

Puedes realizarlo de otra forma en cyberchef con from decimal y to binary


Referencias

https://gchq.github.io/CyberChef/#recipe=From_Base(10)To_Base(2)&input=NDI

https://webshell.picoctf.org