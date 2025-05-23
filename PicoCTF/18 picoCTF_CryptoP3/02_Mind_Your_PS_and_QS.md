Descripción
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/12d820e355a7775a2c9129b2622a7eb6/values)


Hints:
1.⁠ ⁠Bits are expensive, I used only a little bit over 100 to save money

Solución 1

Con terminal linux y python
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 binwalk-env            docProps    fixme1.tar.gz   fixme3                   Music      ppt      shell.php   venv
'[Content_Types].xml'   Documents   fixme2          fixme3.tar.gz            myenv      Public   Templates   Videos
 Desktop                Downloads   fixme2.tar.gz  'Forensics is fun.pptm'   Pictures   _rels   '~.venv'
                                                                                                                           
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Desktop    
                                                                                                                           
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ cd Retos  
                                                                                                                           
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ ls
Actividad_16_cripto1  capture.pcap    crypto2  dolls.jpg  myenv         picopico.key.1  tunn3l_v1s10n.bmp
binwalk               capture.pcap.1  crypto3  Forensic4  picopico.key  TareaForensic3  vulture.jpg
                                                                                                                           
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ cd crypto3
                                                                                                                           
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/crypto3]
└─$ mkdir Mind_Your_PS_and_QS
                                                                                                                           
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/crypto3]
└─$ cd Mind_Your_PS_and_QS 
                                                                                                                           
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/crypto3/Mind_Your_PS_and_QS]
└─$ wget https://mercury.picoctf.net/static/12d820e355a7775a2c9129b2622a7eb6/values    
--2025-05-23 12:16:12--  https://mercury.picoctf.net/static/12d820e355a7775a2c9129b2622a7eb6/values
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 206 [application/octet-stream]
Saving to: ‘values’

values                         100%[===================================================>]     206  --.-KB/s    in 0s      

2025-05-23 12:16:13 (105 MB/s) - ‘values’ saved [206/206]

                                                                                                                           
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/crypto3/Mind_Your_PS_and_QS]
└─$ cat values            
Decrypt my super sick RSA:
c: 843044897663847841476319711639772861390329326681532977209935413827620909782846667
n: 1422450808944701344261903748621562998784243662042303391362692043823716783771691667
e: 65537       
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd desktop/Retos/crypto3/Mind_Your_PS_and_QS
cd: no such file or directory: desktop/Retos/crypto3/Mind_Your_PS_and_QS
                                                                                                                            
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd d                                        
cd: no such file or directory: d
                                                                                                                            
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd r
cd: no such file or directory: r
                                                                                                                            
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd crypto3 
cd: no such file or directory: crypto3
                                                                                                                            
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Desktop                                  
                                                                                                                            
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ cd Retos  
                                                                                                                            
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ cd crypto 
cd: no such file or directory: crypto
                                                                                                                            
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ cd crypto3
                                                                                                                            
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/crypto3]
└─$ cd Mind_Your_PS_and_QS 
                                                                                                                            
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/crypto3/Mind_Your_PS_and_QS]
└─$ python       
Python 3.13.2 (main, Mar 13 2025, 14:29:07) [GCC 14.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> c=843044897663847841476319711639772861390329326681532977209935413827620909782846667
>>> n=1422450808944701344261903748621562998784243662042303391362692043823716783771691667
>>> e=65537
>>> p=2159947535959146091116171018558446546179
>>> q=658558036833541874645521278345168572231473
>>> p*q
1422450808944701344261903748621562998784243662042303391362692043823716783771691667
>>> tn =  ( p-1) *(q-1)
>>> d= pow(e, -1, tn)
>>> m = pow (c,d,n)
>>> m
13016382529449106065927291425342535437996222135352905256639555294957886055592061
>>> bytes.fromhex(hex(m)[2:])
b'picoCTF{sma11_N_n0_g0od_00264570}'
>>> 


picoCTF{sma11_N_n0_g0od_00264570}


Notas adicionales

--------------------


Referencias

terminal linux