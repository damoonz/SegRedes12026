# PW Crack 2
## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.

## Solución
```
damoonz-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.py
--2026-02-16 14:44:30--  https://artifacts.picoctf.net/c/15/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py                    100%[=============================================>]     914  --.-KB/s    in 0s      

2026-02-16 14:44:30 (1.10 GB/s) - 'level2.py' saved [914/914]

damoonz-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
--2026-02-16 14:44:45--  https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc          100%[=============================================>]      31  --.-KB/s    in 0s      

2026-02-16 14:44:45 (1.21 MB/s) - 'level2.flag.txt.enc' saved [31/31]

damoonz-picoctf@webshell:~$ nano level2.py
damoonz-picoctf@webshell:~$ nano level2.py
damoonz-picoctf@webshell:~$ python level2.py
39ce
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
```

picoCTF{tr45h_51ng1ng_502ec42e}

## Notas
## Referencia