# First Grep

## Descripción

Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way.The flag is in this [file](https://challenge-files.picoctf.net/c_fickle_tempest/d0b2e96347614d19414d591c946a1789fa8bd35487fcbfabf9437d0acfcaa503/file).

## Solución -Consola

```
damoonz-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_fickle_tempest/d0b2e96347614d19414d591c946a1789fa8bd35487fcbfabf9437d0acfcaa503/file
--2026-02-09 14:17:33--  https://challenge-files.picoctf.net/c_fickle_tempest/d0b2e96347614d19414d591c946a1789fa8bd35487fcbfabf9437d0acfcaa503/file
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.64, 3.160.5.18, 3.160.5.95, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14546 (14K) [application/octet-stream]
Saving to: 'file'

file                        100%[=========================================>]  14.21K  --.-KB/s    in 0s      

2026-02-09 14:17:34 (360 MB/s) - 'file' saved [14546/14546]

damoonz-picoctf@webshell:~$ cat file | grep "picoCTF" file
```
picoCTF{grep_is_good_to_find_things_e3C4b360}


## Notas
wget - Permite descargar archivos de internet desde la consola
## Referencias
