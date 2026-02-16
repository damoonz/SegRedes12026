
# PW Crack 1

## Descripción

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.
## Solución

```
damoonz-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.py
--2026-02-16 14:39:15--  https://artifacts.picoctf.net/c/12/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py                    100%[=============================================>]     876  --.-KB/s    in 0s      

2026-02-16 14:39:15 (438 MB/s) - 'level1.py' saved [876/876]

damoonz-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
--2026-02-16 14:39:41--  https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.128, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc          100%[=============================================>]      30  --.-KB/s    in 0s      

2026-02-16 14:39:41 (157 KB/s) - 'level1.flag.txt.enc' saved [30/30]

damoonz-picoctf@webshell:~$ cat level1.flag.txt.enc
[gE]__TgS^S

           Jdamoonz-picoctf@webshell:~$ nano level1.py         
damoonz-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 1e1a
That password is incorrect
damoonz-picoctf@webshell:~$ nano level1.py
damoonz-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
```

picoCTF{545h_r1ng1ng_1b2fd683}

## Notas

## Referencias