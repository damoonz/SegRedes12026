## Descripción 
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

Additional details will be available after launching your challenge instance.

## Solución 
```
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ wget 'https://artifacts.picoctf.net/c/164/disk.img.gz'                                                                                            
--2026-03-23 08:19:40--  https://artifacts.picoctf.net/c/164/disk.img.gz
Resolviendo artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.125, 13.225.222.120, 13.225.222.28, ...
Conectando con artifacts.picoctf.net (artifacts.picoctf.net)[13.225.222.125]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 29714372 (28M) [application/octet-stream]
Grabando a: «disk.img.gz»

disk.img.gz                                      100%[==========================================================================================================>]  28.34M  4.61MB/s    en 6.1s    

2026-03-23 08:19:46 (4.66 MB/s) - «disk.img.gz» guardado [29714372/29714372]

                                                                                                                                                                                                    
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ gzip -d disk.img.gz            
                                                                                                                                                                                                    
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ mmls disk.img             
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
                                                                                                                                                                                                    
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ nc saturn.picoctf.net 63371

What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}
```
picoCTF{mm15_f7w!}
## Notas
## Referencias