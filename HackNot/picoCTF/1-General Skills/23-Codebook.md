# Codebook

## Descripción
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/3/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/3/codebook.txt)

## Solución

```
wdamoonz-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/3/codebook.txt
--2026-02-16 14:07:48--  https://artifacts.picoctf.net/c/3/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.128, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                 100%[=============================================>]      27  --.-KB/s    in 0s      

2026-02-16 14:07:48 (552 KB/s) - 'codebook.txt' saved [27/27]

damoonz-picoctf@webshell:~$ ls
README.txt  code.py  codebook.txt  runme.py
damoonz-picoctf@webshell:~$ nano codebook.txt
damoonz-picoctf@webshell:~$ python code.py
picoCTF{c0d3b00k_455157_197a982c}
```
picoCTF{c0d3b00k_455157_197a982c}
## Notas

## Referencias