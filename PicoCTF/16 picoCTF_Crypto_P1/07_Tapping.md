Descripción
Theres tapping coming in from the wires. What's it saying `nc jupiter.challenges.picoctf.org 9422`.

---

Hints:
1.⁠ ⁠What kind of encoding uses dashes and dots?
2.The flag is in the format PICOCTF{}

Solución 1

Con terminal linux

┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Desktop  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ cd Retos  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ ls      
binwalk         dolls.jpg  picopico.key    tunn3l_v1s10n.bmp
capture.pcap    Forensic4  picopico.key.1  vulture.jpg
capture.pcap.1  myenv      TareaForensic3
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ cd Actividad_16_cripto1
cd: no such file or directory: Actividad_16_cripto1
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ mkdir Actividad_16_cripto1
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ cd Actividad_16_cripto1 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1]
└─$ ls
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1]
└─$ mkdir Tapping             
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1]
└─$ cd Ta                  
cd: no such file or directory: Ta
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1]
└─$ cd Tapping 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Actividad_16_cripto1/Tapping]
└─$ nc jupiter.challenges.picoctf.org 9422
.--. .. -.-. --- -.-. - ..-. { -- ----- .-. ... ...-- -.-. ----- -.. ...-- .---- ... ..-. ..- -. ..--- -.... ---.. ...-- ---.. ..--- ....- -.... .---- ----- } 




Respuesta chat
Separando por espacios y decodificando cada parte:

1. Letras antes de la llave `{` (que generalmente indica el inicio de un flag en CTFs):
    
    - `. --.` = P
        
    - `..` = I
        
    - `-.-.` = C
        
    - `---` = O
        
    - `-.-.` = C
        
    - `- ..-.` = T
        
    - `F` (la llave abierta no es parte del Morse, solo marca el formato)
        
    
    Esto forma "PICOCTF{"
    
2. El contenido del flag (números y letras):
    
    - `-- -----` = M 0
        
    - `.-.` = R
        
    - `... ...--` = S 3
        
    - `-.-.` = C
        
    - `-----` = 0
        
    - `-..` = D
        
    - `...--` = 3
        
    - `.--.` = 1
        
    - `...` = S
        
    - `..-.` = F
        
    - `..-` = U
        
    - `-.` = N
        
    - `..---` = 2
        
    - `-....` = 6
        
    - `---..` = 8
        
    - `...--` = 3
        
    - `---..` = 8
        
    - `..---` = 2
        
    - `....-` = 4
        
    - `-....` = 6
        
    - `.---.` = 1
        
    - `-----` = 0
        
3. Combinando todo:  
    PICOCTF{M0RS3C0D31SFUN2683824610}

    PICOCTF{M0RS3C0D31SFUN2683824610}


Notas adicionales

--------------------


Referencias

https://chat.deepseek.com/a/chat/s/86dda463-f7e2-4a8e-b957-f3dd48e2326e

Terminal linux