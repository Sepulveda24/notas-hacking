Descripción
¿Has oído hablar de Rust? ¡Arregla los errores de sintaxis en este archivo Rust para imprimir la bandera!Descargue el código Rust [aquí](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).

Hints:
1.⁠ Cargo es el administrador de paquetes de Rust y te hará la vida más fácil. Vea la página de inicio [aquí](https://doc.rust-lang.org/book/ch01-03-hello-cargo.html)
2.[Impresión!](https://doc.rust-lang.org/std/macro.println.html)
3.Rust tiene algunos mensajes de error del compilador bastante buenos. ¿Quizás los lea?

Solución 1

Con terminal linux

I┌──(parallels㉿kali-linux-2022-2)-[~/fixme1]
└─$ cd src     
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme1/src]
└─$ ls
main.rs
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme1/src]
└─$ nano main.rs     
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme1/src]
└─$ nano main.rs
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme1/src]
└─$ cargo build
   Compiling rust_proj v0.1.0 (/home/parallels/fixme1)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.33s
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme1/src]
└─$ cargo run   
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.01s
     Running `/home/parallels/fixme1/target/debug/rust_proj`



picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}:?
                                   



Notas adicionales

--------------------


Referencias

terminal linux
