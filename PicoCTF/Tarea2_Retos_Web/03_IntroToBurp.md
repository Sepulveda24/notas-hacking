Descripción
Additional details will be available after launching your challenge instance.


Hints:
1.⁠ Try using burpsuite to intercept request to capture the flag.
2.Try mangling the request, maybe their server-side code doesn't handle malformed requests very well.

Solución 1

Con Burpsuite estuve interceptando en la pagina del reto y me llevo hasta la pagina de la contraseña donde me ponia el parametro OTP y eliminando y dando un forward, la transaccion completa y la bandera es capturada


picoCTF{#0TP_Bypvss_SuCc3$S_e1eb16ed}


Notas adicionales

--------------------


Referencias

http://saturn.picoctf.net:58107
https://es.wikipedia.org/wiki/Autenticación_con_contraseña_de_un_solo_uso