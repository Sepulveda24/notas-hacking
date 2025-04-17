Descripción
Can you win in a convincing manner against this chess bot? He won't go easy on you!You can find the challenge [here](http://verbal-sleep.picoctf.net:61344/).

Hints:
1.⁠ ⁠Try understanding the code and how the websocket client is interacting with the server
Solución 1

Con inspeccion de elemento

IEntramos a la página e inspeccionamos el código para ver como funciona.
El codigo utiliza "mate" que indica que Stockfish encontró un jaque mate en una cantidad de jugadas especifica.
Se utiliza "eval" para una evaluación numérica de la posición y se comunica por WebSocket.
Inspeccionamos la página y nos vamos a la consola para enviar un mensaje al servidor WebSocket: 

sendMessage("eval -10000000")


Esto hace que sea una situación muy desfavorable lo cual básicamente significa que la máquina tendrá que rendirse, por lo cual nos muestra lo siguiente:

Huh???? How can I be losing this badly... I resign... here's your flag: picoCTF{c1i3nt_s1d3_w3b_s0ck3t5_a2a9bbe9}




Notas adicionales

--------------------


Referencias

http://verbal-sleep.picoctf.net:61344
