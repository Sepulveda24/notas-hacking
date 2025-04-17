Descripción
There's a flag shop selling stuff, can you buy a flag? [Source](https://jupiter.challenges.picoctf.org/static/253c4651d852ac6342752ff222cf2a83/store.c). Connect with `nc jupiter.challenges.picoctf.org 9745`.

---

Hints:
1.⁠ Two's compliment can do some weird things when numbers get really big!

Solución 1

Con web shell

IEn este reto, se explotó una vulnerabilidad de desbordamiento de enteros (`integer overflow`) al intentar comprar una bandera barata con una cantidad exageradamente grande. Esto provocó que el sistema calculara un costo negativo, aumentando el saldo del usuario a más de 651 millones. Con este saldo inflado, se pudo comprar la bandera real, obteniendo así la flag del reto: `picoCTF{m0n3y_bag5_65d67a74}`.


Notas adicionales

--------------------


Referencias

https://chatgpt.com/c/67fee418-a5e4-8002-adc5-df9f4b6b9530
https://webshell.picoctf.org