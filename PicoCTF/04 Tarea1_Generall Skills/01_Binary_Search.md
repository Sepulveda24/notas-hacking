Descripción
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/4/challenge.zip)

Additional details will be available after launching your challenge instance.

Hints:
1.⁠ Have you ever played hot or cold? Binary search is a bit like that.
2.You have a very limited number of guesses. Try larger jumps between numbers!
3.The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?


Solución 1

Con web shell


fSepulveda24-picoctf@webshell:~/home/ctf-player/drop-in$ nano guessing_game.sh 
Sepulveda24-picoctf@webshell:~/home/ctf-player/drop-in$ ls
guessing_game.sh
Sepulveda24-picoctf@webshell:~/home/ctf-player/drop-in$ cd ..
Sepulveda24-picoctf@webshell:~/home/ctf-player$ ls
drop-in
Sepulveda24-picoctf@webshell:~/home/ctf-player$ cd
Sepulveda24-picoctf@webshell:~$ ls
challenge.zip  home
Sepulveda24-picoctf@webshell:~$ cd home/
Sepulveda24-picoctf@webshell:~/home$ ls
ctf-player
Sepulveda24-picoctf@webshell:~/home$ cd ctf-player/
Sepulveda24-picoctf@webshell:~/home/ctf-player$ ls
drop-in
Sepulveda24-picoctf@webshell:~/home/ctf-player$ cd drop-in/
Sepulveda24-picoctf@webshell:~/home/ctf-player/drop-in$ ls
guessing_game.sh
Sepulveda24-picoctf@webshell:~/home/ctf-player/drop-in$ nanossh -p 64610 ctf-player@atlas.picoctf.net
-bash: nanossh: command not found
Sepulveda24-picoctf@webshell:~/home/ctf-player/drop-in$ ssh -p 64610 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:64610 ([18.217.83.136]:64610)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:64610' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 300
Lower! Try again.
Enter your guess: 200
Lower! Try again.
Enter your guess: 100
Higher! Try again.
Enter your guess: 150
Higher! Try again.
Enter your guess: 170
Lower! Try again.
Enter your guess: 160
Lower! Try again.
Enter your guess: 155
Higher! Try again.
Enter your guess: 156
Higher! Try again.
Enter your guess: 157
Higher! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
Sepulveda24-picoctf@webshell:~/home/ctf-player/drop-in$ ssh -p 64610 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 700
Higher! Try again.
Enter your guess: 800
Lower! Try again.
Enter your guess: 780
Higher! Try again.
Enter your guess: 790
Higher! Try again.
Enter your guess: 795
Lower! Try again.
Enter your guess: 793
Congratulations! You guessed the correct number: 793
Here's your flag: picoCTF{g00d_gu355_ee8225d0}
Connection to atlas.picoctf.net closed.
Sepulveda24-picoctf@webshell:~/home/ctf-player/drop-in$ 
Notas adicionales

-------------

Referencias

https://webshell.picoctf.org