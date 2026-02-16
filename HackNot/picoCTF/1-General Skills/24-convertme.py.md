
# convertme.py

## Descripción
Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)

## Solución
```
damoonz-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2026-02-16 14:12:32--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.16, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                 100%[=============================================>]   1.16K  --.-KB/s    in 0s      

2026-02-16 14:12:33 (456 MB/s) - 'convertme.py' saved [1189/1189]

damoonz-picoctf@webshell:~$ python convertme.py 
If 85 is in decimal base, what is it in binary base?
Answer: 1010101
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
```

picoCTF{4ll_y0ur_b4535_722f6b39}
## Notas

## Referencias