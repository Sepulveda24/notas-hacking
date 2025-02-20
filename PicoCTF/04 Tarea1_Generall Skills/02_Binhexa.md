Descripción
¿Qué tan bien puedes realizar operaciones binarias básicas?Empieza a buscar la bandera aquí`nc titan.picoctf.net 50918`

Hints:
1.⁠(none)

Solución 1

Con web shell y Binary Calculator
Sepulveda24-picoctf@webshell:~$ nc titan.picoctf.net 50918

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 01011010
Binary Number 2: 00011100


Question 1/6:
Operation 1: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0110
Incorrect. Try again
Enter the binary result: 01011110
Correct!

Question 2/6:
Operation 2: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00011000
Correct!

Question 3/6:
Operation 3: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 100111011000
Correct!

Question 4/6:
Operation 4: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 10110100000000000000000000000000000
Incorrect. Try again
Enter the binary result: 10110100000000000000000000000000000
Incorrect. Try again
Enter the binary result: 10110100
Correct!

Question 5/6:
Operation 5: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 1110
Correct!

Question 6/6:
Operation 6: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1110110
Correct!

Enter the results of the last operation in hexadecimal: 76

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_aeaf4b09}




Notas adicionales

-------------

Referencias

https://webshell.picoctf.org


https://www.rapidtables.com/calc/math/binary-calculator.html?num1=01011010&op=0&num2=00011100