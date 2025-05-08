Descripción
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/ac394d24f88e51a09cc909687cf6d853/dds1-alpine.flag.img.gz)
Hints:
1.⁠ Have you ever used `file` to determine what a file was?
2.Relevant terminal-fu in picoGym: https://play.picoctf.org/practice/challenge/85
3Mastering this terminal-fu would enable you to find the flag in a single command: https://play.picoctf.org/practice/challenge/48
4.Using your own computer, you could use qemu to boot from this disk!
Solución 1

Solución 1

Con terminal linux



                                                                            
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ gzip -d dds1-alpine.flag.img.gz 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ ls
concat_v.png  dds1-alpine.flag.img
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ srch_strings dds1-alpine.flag.img                 
RPf1
Missing operating system.
f`f1
|fRfP
Ht[y9Y[
Multiple active partitions.
|XFSBu  f
Operating system load error.
SYSLINUX
PPPP
u%8M
t f=!GPTu
+fRfP
F}+f`f
Boot error
@1,`A1,`
@1,`
(t~k
/os/mnt
@1,`
@1,`@1,`@1,`
@1,`@1,`@1,`
@1,`@1,`@1,`
@1,`@1,`@1,`

┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/Forensic4]
└─$ srch_strings dds1-alpine.flag.img | grep pico
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_dcbf5942}





picoCTF{f0r3ns1c4t0r_n30phyt3_dcbf5942}



Notas adicionales

--------------------


Referencias

https://mercury.picoctf.net/static/ac394d24f88e51a09cc909687cf6d853/dds1-alpine.flag.img.gz