Descripción
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?

Additional details will be available after launching your challenge instance.

Hints:
1.⁠ ⁠XML external entity Injection

Solución 1

Con BurpSuite
En burpsuite se recepto una pagina dandole clic a details donde nos arroja un post, buscando en la documentacion de el link de referencia podemos acceder a /etc/passwd cambiando los parametros para que nos arroje la bandera


Notas adicionales

--------------------


Referencias

https://github.com/payloadbox/xxe-injection-payload-list