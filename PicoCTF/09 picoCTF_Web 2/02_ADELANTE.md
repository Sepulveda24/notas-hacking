Descripción
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:15931/](http://mercury.picoctf.net:15931/)

Hints:
1.⁠ Tal vez tengas más de 2 opciones

2.⁠Echa un vistazo a herramientas como Burpsuite para modificar tus solicitudes y ver las respuestas





Solución 1

Con Burpsuite

Se intercepta cuando le das click a los botones donde uno hace que que el fondo se vuelva rojo y el otro se vuelva azul, con el Burpsuite podemos saber el get y el post para asi considerar el post con le head y conseguir la bandera para resolver el reto

HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_82880908}
Content-type: text/html; charset=UTF-8




Notas adicionales

--------------------

Referencias

https://www.youtube.com/watch?v=GrUuWYwA5l0
https://portswigger.net/burp/community-download-thank-you