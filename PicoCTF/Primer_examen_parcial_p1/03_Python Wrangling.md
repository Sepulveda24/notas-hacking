Descripción
Los scripts de Python se invocan como programas en el Terminal... ¿Puedes ejecutar [este script de Python](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py) usando [esta contraseña](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt) para obtener [la bandera](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en)?

Hints:
1.⁠Obtenga el script de Python accesible en su shell ingresando el siguiente comando en el indicador de la Terminal:`$ wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py`
2.$ man python

Solución 1

Con web shell

Sepulveda24-picoctf@webshell:~$ python ende.py 
Usage: ende.py (-e/-d) [file]
Sepulveda24-picoctf@webshell:~$ python -e ende.py 
Unknown option: -e
usage: python [option] ... [-c cmd | -m mod | file | -] [arg] ...
Try `python -h' for more information.
Sepulveda24-picoctf@webshell:~$ man python
Sepulveda24-picoctf@webshell:~$ python ende.py -d
Please enter the password:
Traceback (most recent call last):
  File "/home/Sepulveda24-picoctf/ende.py", line 44, in <module>
    c = Fernet(ssb_b64)
  File "/usr/local/lib/python3.10/dist-packages/cryptography/fernet.py", line 40, in __init__
    raise ValueError(
ValueError: Fernet key must be 32 url-safe base64-encoded bytes.
Sepulveda24-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt
--2025-04-15 20:23:47--  https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 33 [application/octet-stream]
Saving to: 'pw.txt'

pw.txt                                            100%[===========================================================================================================>]      33  --.-KB/s    in 0s      

2025-04-15 20:23:47 (18.0 MB/s) - 'pw.txt' saved [33/33]

Sepulveda24-picoctf@webshell:~$ ls
README.txt  ende.py  pw.txt
Sepulveda24-picoctf@webshell:~$ open pw.txt 
Sepulveda24-picoctf@webshell:~$ python ende.py -d
Please enter the password:67c6cc9667c6cc9667c6cc9667c6cc96
Traceback (most recent call last):
  File "/home/Sepulveda24-picoctf/ende.py", line 46, in <module>
    with open(sys.argv[2], "r") as f:
IndexError: list index out of range
Sepulveda24-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en
--2025-04-15 20:24:56--  https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 140 [application/octet-stream]
Saving to: 'flag.txt.en'

flag.txt.en                                       100%[===========================================================================================================>]     140  --.-KB/s    in 0s      

2025-04-15 20:24:56 (58.4 MB/s) - 'flag.txt.en' saved [140/140]

Sepulveda24-picoctf@webshell:~$ ls
README.txt  ende.py  flag.txt.en  pw.txt
Sepulveda24-picoctf@webshell:~$ open flag.txt.en 
Warning: unknown mime-type for "flag.txt.en" -- using "application/octet-stream"
Error: no "view" mailcap rules found for type "application/octet-stream"
Sepulveda24-picoctf@webshell:~$ python ende.py -d
Please enter the password:gAAAAABgUAIWsYfVayn4m1dKle5X91HrZW_MIRAW4ILPgf4gD6jalLF4PysYB5_YTpDwclcQPqw_0xTxanpJ_Urx5Vi6mTeBA_rWPA_WQLvVXXHp1mG3EpOgY8Na1_NIAfc9LceH_L2o
Traceback (most recent call last):
  File "/home/Sepulveda24-picoctf/ende.py", line 44, in <module>
    c = Fernet(ssb_b64)
  File "/usr/local/lib/python3.10/dist-packages/cryptography/fernet.py", line 40, in __init__
    raise ValueError(
ValueError: Fernet key must be 32 url-safe base64-encoded bytes.
Sepulveda24-picoctf@webshell:~$ open pw.txt 
Sepulveda24-picoctf@webshell:~$ python ende.py -d flag.txt.en
Please enter the password:67c6cc9667c6cc9667c6cc9667c6cc96



picoCTF{4p0110_1n_7h3_h0us3_67c6cc96}


Notas adicionales

--------------------


Referencias

https://webshell.picoctf.org