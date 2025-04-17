Descripción
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.

Additional details will be available after launching your challenge instance.

Hints:
1.⁠ What programs do you have access to?



Solución 1

Con webshell

Sepulveda24-picoctf@webshell:~$ ssh -p 58328 ctf-player@mimas.picoctf.net
The authenticity of host '[mimas.picoctf.net]:58328 ([52.15.88.75]:58328)' can't be established.
ED25519 key fingerprint is SHA256:n/hDgUtuTTF85Id7k2fxmHvb6rrLrACHNM6xLZ46AqQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? y
Please type 'yes', 'no' or the fingerprint: yes
Warning: Permanently added '[mimas.picoctf.net]:58328' (ED25519) to the list of known hosts.
ctf-player@mimas.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1016-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

SansAlpha$ /*
bash: /bin: Is a directory

SansAlpha$ /*/???[!_]64 */*
/bin/base64: extra operand ‘blargh/flag.txt’
Try '/bin/base64 --help' for more information.

SansAlpha$ /*/???[!_]64 */????.*
cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV8zNmE2NzRjMH0=

SansAlpha$ 
Traceback (most recent call last):
  File "/usr/local/sansalpha.py", line 12, in <module>
    if user_in[-1] != "\n":
IndexError: string index out of range
Connection to mimas.picoctf.net closed.
Sepulveda24-picoctf@webshell:~$ ssh -p 52079 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:52079 ([13.59.203.175]:52079)' can't be established.
ED25519 key fingerprint is SHA256:lMXKIC17ONzyUJx7ZYBY5VSwoxCz20uq5/Nm+IhXKew.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:52079' (ED25519) to the list of known hosts.
ctf-player@saturn.picoctf.net's password: 
Specialer$ help
GNU bash, version 5.0.17(1)-release (x86_64-pc-linux-gnu)
These shell commands are defined internally.  Type `help' to see this list.
Type `help name' to find out more about the function `name'.
Use `info bash' to find out more about the shell in general.
Use `man -k' or `info' to find out more about commands not in this list.

A star (*) next to a name means that the command is disabled.

 job_spec [&]                                       history [-c] [-d offset] [n] or history -anrw [>
 (( expression ))                                   if COMMANDS; then COMMANDS; [ elif COMMANDS; th>
 . filename [arguments]                             jobs [-lnprs] [jobspec ...] or jobs -x command >
 :                                                  kill [-s sigspec | -n signum | -sigspec] pid | >
 [ arg... ]                                         let arg [arg ...]
 [[ expression ]]                                   local [option] name[=value] ...
 alias [-p] [name[=value] ... ]                     logout [n]
 bg [job_spec ...]                                  mapfile [-d delim] [-n count] [-O origin] [-s c>
 bind [-lpsvPSVX] [-m keymap] [-f filename] [-q n>  popd [-n] [+N | -N]
 break [n]                                          printf [-v var] format [arguments]
 builtin [shell-builtin [arg ...]]                  pushd [-n] [+N | -N | dir]
 caller [expr]                                      pwd [-LP]
 case WORD in [PATTERN [| PATTERN]...) COMMANDS ;>  read [-ers] [-a array] [-d delim] [-i text] [-n>
 cd [-L|[-P [-e]] [-@]] [dir]                       readarray [-d delim] [-n count] [-O origin] [-s>
 command [-pVv] command [arg ...]                   readonly [-aAf] [name[=value] ...] or readonly >
 compgen [-abcdefgjksuv] [-o option] [-A action] >  return [n]
 complete [-abcdefgjksuv] [-pr] [-DEI] [-o option>  select NAME [in WORDS ... ;] do COMMANDS; done
 compopt [-o|+o option] [-DEI] [name ...]           set [-abefhkmnptuvxBCHP] [-o option-name] [--] >
 continue [n]                                       shift [n]
 coproc [NAME] command [redirections]               shopt [-pqsu] [-o] [optname ...]
 declare [-aAfFgilnrtux] [-p] [name[=value] ...]    source filename [arguments]
 dirs [-clpv] [+N] [-N]                             suspend [-f]
 disown [-h] [-ar] [jobspec ... | pid ...]          test [expr]
 echo [-neE] [arg ...]                              time [-p] pipeline
 enable [-a] [-dnps] [-f filename] [name ...]       times
 eval [arg ...]                                     trap [-lp] [[arg] signal_spec ...]
 exec [-cl] [-a name] [command [arguments ...]] [>  true
 exit [n]                                           type [-afptP] name [name ...]
 export [-fn] [name[=value] ...] or export -p       typeset [-aAfFgilnrtux] [-p] name[=value] ...
 false                                              ulimit [-SHabcdefiklmnpqrstuvxPT] [limit]
 fc [-e ename] [-lnr] [first] [last] or fc -s [pa>  umask [-p] [-S] [mode]
 fg [job_spec]                                      unalias [-a] name [name ...]
 for NAME [in WORDS ... ] ; do COMMANDS; done       unset [-f] [-v] [-n] [name ...]
 for (( exp1; exp2; exp3 )); do COMMANDS; done      until COMMANDS; do COMMANDS; done
 function name { COMMANDS ; } or name () { COMMAN>  variables - Names and meanings of some shell va>
 getopts optstring name [arg]                       wait [-fn] [id ...]
 hash [-lr] [-p pathname] [-dt] [name ...]          while COMMANDS; do COMMANDS; done
 help [-dms] [pattern ...]                          { COMMANDS ; }
Specialer$ echo *
abra ala sim
Specialer$ echo .* *
. .. .hushlogin .profile abra ala sim
Specialer$ echo .* */*
. .. .hushlogin .profile abra/cadabra.txt abra/cadaniel.txt ala/kazam.txt ala/mode.txt sim/city.txt sim/salabim.txt
Specialer$ cho .* */*
-bash: cho: command not found
Specialer$ 
Specialer$ echo .* */*
. .. .hushlogin .profile abra/cadabra.txt abra/cadaniel.txt ala/kazam.txt ala/mode.txt sim/city.txt sim/salabim.txt
Specialer$ echo "$(<abra/cadabra.txt)"
Nothing up my sleeve!
Specialer$ echo "$(<abra/cadaniel.txt)"
Yes, I did it! I really did it! I'm a true wizard!
Specialer$ echo "$(<ala/kazam.txt)"
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_38f5cc78}"

Specialer$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.



picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_38f5cc78}


Notas adicionales

--------------------


Referencias

https://webshell.picoctf.org 