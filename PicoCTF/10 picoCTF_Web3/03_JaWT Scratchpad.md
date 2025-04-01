Descripción
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/58210/`or http://jupiter.challenges.picoctf.org:58210
Hints:
1.⁠ ¿Qué es esa galleta?
2.¿Has oído hablar de JWT?

Solución 1

Con cookie editor

me logeo en la pagina indicada del reto donde comienzo a investigar y con cookie editor decodifico la cookie de la pagina logeado, donde pide agregar un codigo secreto, que se saca con la consola y te da ilovepico, si agregas esa palabra secreta a la cookie decodificada y cambias ael usuario a admin, refrescando la página descubres la bandera.

picoCTF{3v3ry1_l0v3s_c00k135_88acab36}


Notas adicionales

--------------------


Referencias

https://es.wikipedia.org/wiki/JSON
https://jupiter.challenges.picoctf.org/problem/58210/
https://jwt.io