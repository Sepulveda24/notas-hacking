Descripción
¡Encuentra la bandera en el script de Python![Descargar script de Python](https://artifacts.picoctf.net/c/35/serpentine.py)

Hints:
1.⁠ Intenta ejecutar el script y mira qué pasa
2.En el webshell, intenta examinar el script con un editor de texto como`nano`
3.Para salir de `nano`, presione Ctrl y x y siga las indicaciones en pantalla
4.The `str_xor` function does not need to be reverse engineered for this challenge.


Solución 1

Con web shell


Sepulveda24-picoctf@webshell:~$ rm -rf *
Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.py
--2025-02-20 18:59:03--  https://artifacts.picoctf.net/c/18/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.93, 3.160.5.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py                                         100%[===========================================================================================================>]   1.31K  --.-KB/s    in 0s      

2025-02-20 18:59:03 (828 MB/s) - 'level3.py' saved [1337/1337]

Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
--2025-02-20 18:59:23--  https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.71, 3.160.5.18, ...
Sepulveda24-picoctf@webshell:~$  https://artifacts.picoctf.net/c/35/serpentine.py
-bash: https://artifacts.picoctf.net/c/35/serpentine.py: No such file or directory
Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/35/serpentine.py
--2025-02-20 19:08:26--  https://artifacts.picoctf.net/c/35/serpentine.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.18, 3.160.5.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2550 (2.5K) [application/octet-stream]
Saving to: 'serpentine.py'

serpentine.py                                     100%[===========================================================================================================>]   2.49K  --.-KB/s    in 0s      

2025-02-20 19:08:26 (48.2 MB/s) - 'serpentine.py' saved [2550/2550]

Sepulveda24-picoctf@webshell:~$ ls
level3.flag.txt.enc  level3.hash.bin  level3.py  serpentine.py
Sepulveda24-picoctf@webshell:~$ python serpentine.py 

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b

Oops! I must have misplaced the print_flag function! Check my source code!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) c
Sepulveda24-picoctf@webshell:~$ nano serpentine.py 
Sepulveda24-picoctf@webshell:~$ python serpentine.py 

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) c
Sepulveda24-picoctf@webshell:~$ 

Notas adicionales

-------------

Referencias

https://webshell.picoctf.org