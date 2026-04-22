## Descripción 
How about some hide and seek heh? Look at this image [here](https://artifacts.picoctf.net/c/239/atbash.jpg).
## Solución 

```
──(moonz㉿damoonz)-[~/Documentos/picoctf]
└─$ wget 'https://artifacts.picoctf.net/c/239/atbash.jpg' 
--2026-04-22 08:32:55--  https://artifacts.picoctf.net/c/239/atbash.jpg
Resolviendo artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.105, 13.225.222.120, 13.225.222.125, ...
Conectando con artifacts.picoctf.net (artifacts.picoctf.net)[13.225.222.105]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 51504 (50K) [application/octet-stream]
Grabando a: «atbash.jpg»

atbash.jpg              100%[==============================>]  50.30K   113KB/s    en 0.4s    

2026-04-22 08:32:59 (113 KB/s) - «atbash.jpg» guardado [51504/51504]

                                                                                               
┌──(moonz㉿damoonz)-[~/Documentos/picoctf]
└─$ steghide --extract -sf atbash.jpg 
Anotar salvoconducto: 
anot� los datos extra�dos e/"encrypted.txt".
                                                                                               
┌──(moonz㉿damoonz)-[~/Documentos/picoctf]
└─$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_1u84w779}



```
https://gchq.github.io/CyberChef/#recipe=Atbash_Cipher()&input=a3J4bFhHVXt6Z3l6aHNfeGl6eHBfMXU4NHc3Nzl9Cg


picoCTF{atbash_crack_1f84d779}

## Notas
## Referencias