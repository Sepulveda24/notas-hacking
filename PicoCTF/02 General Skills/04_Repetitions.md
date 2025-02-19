Descripción
Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/474/enc_flag).

Hints:
1.Multiple decoding is always good.
Solución 1

Con webshell
Sepulveda24-picoctf@webshell:~/big-zip-files$ cd
Sepulveda24-picoctf@webshell:~$ ls
README.txt  big-zip-files  big-zip-files.zip  files  files.zip
Sepulveda24-picoctf@webshell:~$ rm -rf
Sepulveda24-picoctf@webshell:~$ ls
README.txt  big-zip-files  big-zip-files.zip  files  files.zip
Sepulveda24-picoctf@webshell:~$ rm -rf *
Sepulveda24-picoctf@webshell:~$ ls
Sepulveda24-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/474/enc_flag
--2025-02-18 19:33:25--  https://artifacts.picoctf.net/c/474/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 349 [application/octet-stream]
Saving to: 'enc_flag'

enc_flag                                          100%[===========================================================================================================>]     349  --.-KB/s    in 0s      

2025-02-18 19:33:25 (3.55 MB/s) - 'enc_flag' saved [349/349]

Sepulveda24-picoctf@webshell:~$ ls
enc_flag
Sepulveda24-picoctf@webshell:~$ cd enc_flag
-bash: cd: enc_flag: Not a directory
Sepulveda24-picoctf@webshell:~$ ls -l
total 4
-rw-rw-r-- 1 Sepulveda24-picoctf Sepulveda24-picoctf 349 Mar 16  2023 enc_flag
Sepulveda24-picoctf@webshell:~$ chmod -x enc_flag 
Sepulveda24-picoctf@webshell:~$ ls
enc_flag
Sepulveda24-picoctf@webshell:~$ ls -l
total 4
-rw-rw-r-- 1 Sepulveda24-picoctf Sepulveda24-picoctf 349 Mar 16  2023 enc_flag
Sepulveda24-picoctf@webshell:~$ cat enc_flag 
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZhTTBKUFdXdGtlbVF4V2tkWGJYUllDbUY2UWpSWmEyaFRWakpHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
Sepulveda24-picoctf@webshell:~$ picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_3f81f7be}

Usando  cyberchef
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Vm1wR1UxRXlSWGxVV0d4VFlteEtWVll3WkZOV2JHeHlWMjFHVjFKdGVEQlViRnBQWVd4S2RGVnNhRnBXVmxVeFdWWmFTMVpXV25WaApSbVJYWld0YWIxZFdXbXRTTWs1eVRsWldXQXBpVlZwVVZtMTBkMVZXWkZkVmEyUnBZbFphV0ZadE5WZFZaM0JwVTBWS2VsZFdVa05rCk1sWlhWbGhvV0dKWVFrOVZiRkpYVTBaa2NWUnVUbGRhTTBKWlZXcEdTMlZXV2tkYVNHUlhDazFzV25wV1YzaGhWbTFLUms1WE9WVlcKVmtwRVZHeGFZVmRGTVZoU2JGWmhUVEJLVUZkWGRHdGxiVkY0VjJ0a1dHSllVbGxEYlVZMlVXcFNXbUV5YUZSV2FrcEhaRWRXUmxacwphR2tLWWxScmVsWkVSbGRVTWtwelVXeFdUbEpZVGt4RFp6MDlDZz09

'''
Input: VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZhTTBKUFdXdGtlbVF4V2tkWGJYUllDbUY2UWpSWmEyaFRWakpHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
Recipe: 
from base  64
from base  64
from base  64
from base  64
from base  64
from base  64
Output: picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_3f81f7be}

'''




Notas adicionales

-------------

Referencias

https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Vm1wR1UxRXlSWGxVV0d4VFlteEtWVll3WkZOV2JHeHlWMjFHVjFKdGVEQlViRnBQWVd4S2RGVnNhRnBXVmxVeFdWWmFTMVpXV25WaApSbVJYWld0YWIxZFdXbXRTTWs1eVRsWldXQXBpVlZwVVZtMTBkMVZXWkZkVmEyUnBZbFphV0ZadE5WZFZaM0JwVTBWS2VsZFdVa05rCk1sWlhWbGhvV0dKWVFrOVZiRkpYVTBaa2NWUnVUbGRhTTBKWlZXcEdTMlZXV2tkYVNHUlhDazFzV25wV1YzaGhWbTFLUms1WE9WVlcKVmtwRVZHeGFZVmRGTVZoU2JGWmhUVEJLVUZkWGRHdGxiVkY0VjJ0a1dHSllVbGxEYlVZMlVXcFNXbUV5YUZSV2FrcEhaRWRXUmxacwphR2tLWWxScmVsWkVSbGRVTWtwelVXeFdUbEpZVGt4RFp6MDlDZz09
https://webshell.picoctf.org