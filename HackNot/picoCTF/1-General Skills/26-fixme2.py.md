

# fixme2.py
## Descripción
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/4/fixme2.py)

## Solución

```
damoonz-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/4/fixme2.py
--2026-02-16 14:36:24--  https://artifacts.picoctf.net/c/4/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                    100%[=============================================>]   1.00K  --.-KB/s    in 0s      

2026-02-16 14:36:24 (403 MB/s) - 'fixme2.py' saved [1029/1029]

damoonz-picoctf@webshell:~$ python fixme2.py 
  File "/home/damoonz-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
damoonz-picoctf@webshell:~$ nano fixme2.py 
damoonz-picoctf@webshell:~$ nano fixme2.py 
damoonz-picoctf@webshell:~$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
```
picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}

## Notas
## Referencias
