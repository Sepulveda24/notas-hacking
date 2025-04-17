Descripción
BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!

Additional details will be available after launching your challenge instance.

Hints:
1.⁠ ⁠Maybe try to find the JWT Signing Key ("secret key") in the source code? Maybe it's hardcoded somewhere? Or maybe try to crack it?
2.The 'role' and 'userId' fields in the JWT can be of interest to you!
3.The 'controllers', 'services' and 'security' java packages in the given source code might need your attention. We've provided a README.md file that contains some documentation.
4.Upgrade your 'role' with the _new_(cracked) JWT. And re-login for the new role to get reflected in browser's localStorage.



Solución 1

Con inspeccion de elementos

Al entrar al servidor observamos una imagen FLAG restringida a la que solo se puede acceder como Admin.
Inspeccionamos la imagen para sacar el token y cambiar lo necesario para encontrar la bandera
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiQWRtaW4iLCJpc3MiOiJib29rc2hlbGYiLCJleHAiOjE3NDU0MjE5MDksImlhdCI6MTc0NDgxNzEwOSwidXNlcklkIjoyLCJlbWFpbCI6ImFkbWluIn0.6wT4uq_SDs94g0r4a1zXgKVDVkyV9Bk4_iuW8A99BK4, al cambiar esto en el valor del servidor y recargar la pagina te devuelve la bandera



picoCTF{w34k_jwt_n0t_g00d_602ce414}


Notas adicionales

--------------------


Referencias

http://saturn.picoctf.net:58250/#/pdf
https://jwt.io