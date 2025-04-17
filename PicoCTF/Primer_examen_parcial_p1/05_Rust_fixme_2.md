Descripción
The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz).

Hints:
1.⁠ ⁠(https://doc.rust-lang.org/book/ch04-02-references-and-borrowing.html

Solución 1

Con terminal linux

┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ wget https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz
--2025-04-15 16:20:41--  https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 65.9.149.85, 65.9.149.24, 65.9.149.59, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|65.9.149.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1585 (1.5K) [application/octet-stream]
Saving to: ‘fixme2.tar.gz’

fixme2.tar.gz       100%[================>]   1.55K  --.-KB/s    in 0s      

2025-04-15 16:20:46 (24.7 MB/s) - ‘fixme2.tar.gz’ saved [1585/1585]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 Desktop     Downloads       fixme2.tar.gz   Pictures   Templates   Videos
 Documents   fixme1.tar.gz   Music           Public    '~.venv'
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ tar -xvf fixme2.tar.gz
fixme2/
fixme2/Cargo.toml
fixme2/Cargo.lock
fixme2/src/
fixme2/src/main.rs
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 Desktop     Downloads       fixme2          Music      Public     '~.venv'
 Documents   fixme1.tar.gz   fixme2.tar.gz   Pictures   Templates   Videos
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd fixme2 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme2]
└─$ ls
Cargo.lock  Cargo.toml  src
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme2]
└─$ cd src   
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme2/src]
└─$ rustc --version
rustc 1.85.0 (4d91de4e4 2025-02-17) (built from a source tarball)
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme2/src]
└─$ cd .. 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme2]
└─$ cargo build 
   Compiling crossbeam-utils v0.8.20
   Compiling rayon-core v1.12.1
   Compiling either v1.13.0
   Compiling crossbeam-epoch v0.9.18
   Compiling crossbeam-deque v0.8.5
   Compiling rayon v1.10.0
   Compiling xor_cryptor v1.2.3
   Compiling rust_proj v0.1.0 (/home/parallels/fixme2)
error[E0596]: cannot borrow `*borrowed_string` as mutable, as it is behind a `&` reference
 --> src/main.rs:9:5
  |
9 |     borrowed_string.push_str("PARTY FOUL! Here is your flag: ");
  |     ^^^^^^^^^^^^^^^ `borrowed_string` is a `&` reference, so the data it refers to cannot be borrowed as mutable                                      
  |
help: consider changing this to be a mutable reference
  |
3 | fn decrypt(encrypted_buffer:Vec<u8>, borrowed_string: &mut String){ // How do we pass values to a function that we want to change?
  |                                                        +++

error[E0596]: cannot borrow `*borrowed_string` as mutable, as it is behind a `&` reference
  --> src/main.rs:20:5
   |
20 |     borrowed_string.push_str(&String::from_utf8_lossy(&decrypted_buff...
   |     ^^^^^^^^^^^^^^^ `borrowed_string` is a `&` reference, so the data it refers to cannot be borrowed as mutable                                     
   |
help: consider changing this to be a mutable reference
   |
3  | fn decrypt(encrypted_buffer:Vec<u8>, borrowed_string: &mut String){ // How do we pass values to a function that we want to change?
   |                                                        +++

For more information about this error, try `rustc --explain E0596`.
error: could not compile `rust_proj` (bin "rust_proj") due to 2 previous errors
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme2]
└─$ cd src     
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme2/src]
└─$ nano main.rs 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme2/src]
└─$ cargo build 
   Compiling rust_proj v0.1.0 (/home/parallels/fixme2)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.34s
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/fixme2/src]
└─$ cargo run  
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.01s
     Running `/home/parallels/fixme2/target/debug/rust_proj`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: 

picoCTF{4r3_y0u_h4v1n5_fun_y31?}




Notas adicionales

--------------------


Referencias
https://doc.rust-lang.org/book/ch04-02-references-and-borrowing.html 