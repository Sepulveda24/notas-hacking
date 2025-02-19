Descripcion
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 15130`.



Hints:

1.I hear python can convert things.
2.It might help to have multiple windows open.

Solución 1
con web shell

Sepulveda24-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 15130.
nc: port number invalid: 15130.
Sepulveda24-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 15130 
Let us see how data is stored
chair
Please give the 01100011 01101000 01100001 01101001 01110010 as a word.
...
you have 45 seconds.....

Input:
chair
Please give me the  154 151 172 141 162 144 as a word.
Input:
lizard
Please give me the 66616c636f6e as a word.
Input:
falcon
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_02167de8}

Descripción
Can you convert the number 42 (base 10) to binary (base 2)?

Hints:
1.⁠ ⁠Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.







Solución 2
Usando cyberchef https://gchq.github.io/CyberChef/#recipe=From_Hex('None')&input=NjY2MTZjNjM2ZjZl


https://gchq.github.io/CyberChef/#recipe=From_Octal('Space')&input=MTU0IDE1MSAxNzIgMTQxIDE2MiAxNDQ

'''
Input: 154 151 172 141 162 144
Recipe: from octal  
Output: lizard
'''

'''
Input: 66616c636f6e
Recipe: from hex  
Output: falcon
'''

Notas adicionales


Referencias

https://gchq.github.io/CyberChef/#recipe=From_Hex('None')&input=NjY2MTZjNjM2ZjZl


https://gchq.github.io/CyberChef/#recipe=From_Octal('Space')&input=MTU0IDE1MSAxNzIgMTQxIDE2MiAxNDQ

https://webshell.picoctf.org