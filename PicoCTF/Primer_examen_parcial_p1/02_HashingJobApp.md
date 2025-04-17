Descripción
¿Qué tal si intentas hacer coincidir una expresión normal?El sitio web está funcionando [aquí](http://saturn.picoctf.net:58107/).


Hints:
1.⁠ ⁠You can use a commandline tool or web app to hash text
2.You can use a commandline tool or web app to hash text


Solución 1

Con webshell y cyberchef

Sepulveda24-picoctf@webshell:~$ nc saturn.picoctf.net 55452
Please md5 hash the text between quotes, excluding the quotes: 'Backstreet Boys'
Answer: 


Incorrect. Try again?
Answer: 
340af906f373c781bb56e2e1b51bc325
340af906f373c781bb56e2e1b51bc325
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'hairballs'
Answer: 
1069a9d2f582b54f19c97b79c49d1069
1069a9d2f582b54f19c97b79c49d1069
Incorrect. Try again?
Answer: 
360927e98748b8675251a4a68b637b4b
360927e98748b8675251a4a68b637b4b
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'gravity'
Answer: 
67f2a835697e7c9c2c5146c76eca6038
67f2a835697e7c9c2c5146c76eca6038
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_3eb82b73}

picoCTF{4ppl1c4710n_r3c31v3d_3eb82b73}


Iba introduciendo las palabras como especifica en la instruccion con md5 para pasar los filtros y econtrar las banderas

Notas adicionales

--------------------


Referencia

https://webshell.picoctf.org