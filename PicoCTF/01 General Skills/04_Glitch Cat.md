Descripción
Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance.


Hints:
1.⁠ ⁠ASCII is one of the most common encodings used in programming
2.We know that the glitch output is valid Python, somehow!
3.Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

Solución 1
Con Python
┌──(parallels㉿kali-linux-2022-2)-[~/Downloads]
└─$ python                           
Python 3.10.5 (main, Jun  8 2022, 09:26:22) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
KeyboardInterrupt
>>> picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
  File "<stdin>", line 1
    picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
           ^
SyntaxError: invalid syntax
>>> picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'exit
  File "<stdin>", line 1
    picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'exit
           ^
SyntaxError: invalid syntax
>>> d
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'd' is not defined. Did you mean: 'id'?
>>> 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Downloads]
└─$ python3
Python 3.10.5 (main, Jun  8 2022, 09:26:22) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
KeyboardInterrupt
>>> picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
  File "<stdin>", line 1
    picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
           ^
SyntaxError: invalid syntax
>>> chr(0x61) 
'a'
>>> chr(0x34)
'4'
>>> chr(0x33)
'3'
>>> chr(0x39)
'9'
>>> chr(0x32)
'2'
>>> chr(0x64)
'd'
>>> chr(0x32)]
  File "<stdin>", line 1
    chr(0x32)]
             ^
SyntaxError: unmatched ']'
>>> chr(0x32)
'2'
>>> chr(0x65)
'e'
>>> picoCTF{gl17ch_m3_n07_a4392d2e}

Solucion 2
con cyberchef https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=KDB4NjEpIAoKKDB4MzQpCgooMHgzMykKCigweDM5KQoKKDB4MzIpCgooMHg2NCkKCigweDMyKQoKKDB4NjUp&oenc=65001

'''
Input: (0x61) 

(0x34)

(0x33)

(0x39)

(0x32)

(0x64)

(0x32)

(0x65)
Recipe: From Hex
Output: a4392d2e
'''


Notas adicionales


Referenciascon cyberchef https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=KDB4NjEpIAoKKDB4MzQpCgooMHgzMykKCigweDM5KQoKKDB4MzIpCgooMHg2NCkKCig