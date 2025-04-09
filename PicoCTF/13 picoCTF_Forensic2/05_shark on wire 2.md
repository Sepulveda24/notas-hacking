Descripción
Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.
Hints:
1.⁠ ⁠How did pictures from the moon landing get sent back to Earth?
2.What is the CMU mascot?, that might help select a RX option

Solución 1

Con TerminalLinux
                                                                             ┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ pythoon3               
Command 'pythoon3' not found, did you mean:
  command 'python3' from deb python3-minimal
Try: sudo apt install <deb name>
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ python3                
Python 3.10.5 (main, Jun  8 2022, 09:26:22) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(112)
'p'
>>> chr(105)
'i'
>>> chr(123)
'{'
>>> chr(112)
'p'
>>> chr(049)
  File "<stdin>", line 1
    chr(049)
        ^
SyntaxError: leading zeros in decimal integer literals are not permitted; use an 0o prefix for octal integers
>>> chr(49)
'1'
>>> chr(76)
'L'
>>> chr(76)
'L'
>>> chr(102)
'f'
>>> chr(51)
'3'
>>> chr(114)
'r'
>>> chr(51)
'3'
>>> chr(100)
'd'
>>> chr(95)
'_'
>>> chr(100)
'd'
>>> chr(97)
'a'
>>> chr(116)
't'
>>> chr(97)
'a'
>>> chr(95)
'_'
>>> chr(118)
'v'
>>> chr(49)
'1'
>>> chr(97)
'a'
>>> chr(95)
'_'
>>> chr(115)
's'
>>> chr(116)
't'
>>> chr(51)
'3'
>>> chr(103)
'g'
>>> chr(48)
'0'
>>> chr(125)
'}'
>>> 
KeyboardInterrupt
>>> 



Notas adicionales

--------------------


Referencias

terminalLinux