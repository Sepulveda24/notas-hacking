Descripción
¡Mi equipo ha estado trabajando muy duro en nuevas características para nuestro programa de impresión de banderas! Me pregunto cómo trabajarán juntos.Puedes descargar los archivos del desafío aquí:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/71/challenge.zip)

Hints:
1.⁠ ⁠`git branch -a`te dejará ver las sucursales disponibles
2¿Cómo se pueden llevar los archivos 'diffs' a la sucursal principal? ¡No te olvides de `git config`!
3.¡Fusión de conflictos puede ser complicado! Prueba con un editor de texto como nano, emacs o vim.

Solución 1

Con web shell

Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/71/challenge.zip
--2025-02-20 20:21:46--  https://artifacts.picoctf.net/c_titan/71/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.18, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 24467 (24K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                     100%[===========================================================================================================>]  23.89K  --.-KB/s    in 0.004s  

2025-02-20 20:21:46 (5.65 MB/s) - 'challenge.zip' saved [24467/24467]

Sepulveda24-picoctf@webshell:~$ ls
challenge.zip
Sepulveda24-picoctf@webshell:~$ unzip
UnZip 6.00 of 20 April 2009, by Debian. Original by Info-ZIP.

Usage: unzip [-Z] [-opts[modifiers]] file[.zip] [list] [-x xlist] [-d exdir]
  Default action is to extract files in list, except those in xlist, to exdir;
  file[.zip] may be a wildcard.  -Z => ZipInfo mode ("unzip -Z" for usage).

  -p  extract files to pipe, no messages     -l  list files (short format)
  -f  freshen existing files, create none    -t  test compressed archive data
  -u  update files, create if necessary      -z  display archive comment only
  -v  list verbosely/show version info       -T  timestamp archive to latest
  -x  exclude files that follow (in xlist)   -d  extract files into exdir
modifiers:
  -n  never overwrite existing files         -q  quiet mode (-qq => quieter)
  -o  overwrite files WITHOUT prompting      -a  auto-convert any text files
  -j  junk paths (do not make directories)   -aa treat ALL files as text
  -U  use escapes for all non-ASCII Unicode  -UU ignore any Unicode fields
  -C  match filenames case-insensitively     -L  make (some) names lowercase
  -X  restore UID/GID info                   -V  retain VMS version numbers
  -K  keep setuid/setgid/tacky permissions   -M  pipe through "more" pager
  -O CHARSET  specify a character encoding for DOS, Windows and OS/2 archives
  -I CHARSET  specify a character encoding for UNIX and other archives

See "unzip -hh" or unzip.txt for more help.  Examples:
  unzip data1 -x joe   => extract all files except joe from zipfile data1.zip
  unzip -p foo | more  => send contents of foo.zip via pipe into program more
  unzip -fo foo ReadMe => quietly replace existing ReadMe if archive file newer
Sepulveda24-picoctf@webshell:~$ unzip challenge.zip 
Archive:  challenge.zip
   creating: drop-in/
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/main  
   creating: drop-in/.git/refs/heads/feature/
  inflating: drop-in/.git/refs/heads/feature/part-1  
 extracting: drop-in/.git/refs/heads/feature/part-2  
 extracting: drop-in/.git/refs/heads/feature/part-3  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/77/
 extracting: drop-in/.git/objects/77/d6ceca6fe23b57d88cf16f20003e10d6715690  
   creating: drop-in/.git/objects/b9/
 extracting: drop-in/.git/objects/b9/32e8c048154a46d224cd7691c99dc8cb88164a  
   creating: drop-in/.git/objects/6c/
 extracting: drop-in/.git/objects/6c/e09adec311b859780caf89d993c58e34b53fa6  
   creating: drop-in/.git/objects/6e/
 extracting: drop-in/.git/objects/6e/17fb3a35364b4f9bb8bef8b5e6a5af2d3e7dfa  
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/e44dd37ba0c0adc3d78d0b85d699859ec8d75c  
   creating: drop-in/.git/objects/74/
 extracting: drop-in/.git/objects/74/ae5215b93a82ddf3dd37df3d4c6b5aff0a93ed  
   creating: drop-in/.git/objects/7a/
 extracting: drop-in/.git/objects/7a/b4e25c0cd108374b2275fdb1fcdf635e591833  
   creating: drop-in/.git/objects/d1/
 extracting: drop-in/.git/objects/d1/f3407cee4479c075997b497fa290ca636fe258  
   creating: drop-in/.git/objects/b4/
 extracting: drop-in/.git/objects/b4/612c914d8461d1b1a50652cc303b76813ee142  
 extracting: drop-in/.git/objects/b4/5df8ce6725e05ed8f45745793f91c26f6529dc  
   creating: drop-in/.git/objects/59/
 extracting: drop-in/.git/objects/59/d9bf3f55055654fda549be87499374805f28e3  
   creating: drop-in/.git/objects/5c/
 extracting: drop-in/.git/objects/5c/6d493ac583a95117d3a70eb5b10d9d76991c48  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/main  
   creating: drop-in/.git/logs/refs/heads/feature/
  inflating: drop-in/.git/logs/refs/heads/feature/part-1  
  inflating: drop-in/.git/logs/refs/heads/feature/part-2  
  inflating: drop-in/.git/logs/refs/heads/feature/part-3  
  inflating: drop-in/flag.py         
Sepulveda24-picoctf@webshell:~$ ls
challenge.zip  drop-in
Sepulveda24-picoctf@webshell:~$ cd dr
-bash: cd: dr: No such file or directory
Sepulveda24-picoctf@webshell:~$ cd drop-in/
Sepulveda24-picoctf@webshell:~/drop-in$ ls
flag.py
Sepulveda24-picoctf@webshell:~/drop-in$ python flag.py 
Printing the flag...
Sepulveda24-picoctf@webshell:~/drop-in$ git branch -a
Sepulveda24-picoctf@webshell:~/drop-in$ git merge
fatal: No remote for the current branch.
Sepulveda24-picoctf@webshell:~/drop-in$ git branch -a
Sepulveda24-picoctf@webshell:~/drop-in$ git merge feature/part-1
Updating 6ce09ad..74ae521
Fast-forward
 flag.py | 1 +
 1 file changed, 1 insertion(+)
Sepulveda24-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')Sepulveda24-picoctf@webshell:~/drop-in$ git merge feature/part-2
Committer identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'Sepulveda24-picoctf@webshell.(none)')
Sepulveda24-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')Sepulveda24-picoctf@webshell:~/drop-in$ git config --global user.name random
Sepulveda24-picoctf@webshell:~/drop-in$ ls
flag.py
Sepulveda24-picoctf@webshell:~/drop-in$ git config --global user.email random@gmail.com
Sepulveda24-picoctf@webshell:~/drop-in$ git merge feature/part-2
Auto-merging flag.py
CONFLICT (content): Merge conflict in flag.py
Automatic merge failed; fix conflicts and then commit the result.
Sepulveda24-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")
<<<<<<< HEAD
print("picoCTF{t3@mw0rk_", end='')
=======

print("m@k3s_th3_dr3@m_", end='')
>>>>>>> feature/part-2
Sepulveda24-picoctf@webshell:~/drop-in$ git add flag.py 
Sepulveda24-picoctf@webshell:~/drop-in$ git commit -m "mezcla"
[main e44bff3] mezcla
Sepulveda24-picoctf@webshell:~/drop-in$ git merge feature/part-3
Auto-merging flag.py
CONFLICT (content): Merge conflict in flag.py
Automatic merge failed; fix conflicts and then commit the result.
Sepulveda24-picoctf@webshell:~/drop-in$ git add flag.py 
Sepulveda24-picoctf@webshell:~/drop-in$ git commit -m "mezcla2"
[main 025316a] mezcla2
Sepulveda24-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")
<<<<<<< HEAD
<<<<<<< HEAD
print("picoCTF{t3@mw0rk_", end='')
=======

print("m@k3s_th3_dr3@m_", end='')
>>>>>>> feature/part-2
=======

print("w0rk_4c24302f}")
>>>>>>> feature/part-3

Notas adicionales

-------------

Referencias

https://webshell.picoctf.org
https://primer.picoctf.org/#_git_version_control