# fixme1.py

## Descripción
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)
## Solución
```
damoonz-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/26/fixme1.py
--2026-02-16 14:28:19--  https://artifacts.picoctf.net/c/26/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py                                                  100%[========================================================================================================================================>]     837  --.-KB/s    in 0s      

2026-02-16 14:28:19 (58.0 MB/s) - 'fixme1.py' saved [837/837]

damoonz-picoctf@webshell:~$ nano fixme1.py 
damoonz-picoctf@webshell:~$ python fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}
```

picoCTF{1nd3nt1ty_cr1515_09ee727a}
## Notas
-q (quiet, no da especificaciones del comando)
## Referencias