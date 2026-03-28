## Descripción 
Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/258/flag.png).
## Solución 

Viendo la información del archivo se puede ver que hay archivos ocultos, se descomprimen y se abre la imagen que contiene la bandera y se copia la flag.
```
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ xxd flag.png | tail             
0000a720: 0000 0000 0000 0010 00ed 4100 0000 0073  ..........A....s
0000a730: 6563 7265 742f 5554 0500 038d 7812 6475  ecret/UT....x.du
0000a740: 780b 0001 0400 0000 0004 0000 0000 504b  x.............PK
0000a750: 0102 1e03 1400 0000 0800 3910 7056 0f5a  ..........9.pV.Z
0000a760: d178 3c0b 0000 d50b 0000 0f00 1800 0000  .x<.............
0000a770: 0000 0000 0000 a481 4100 0000 7365 6372  ........A...secr
0000a780: 6574 2f66 6c61 672e 706e 6755 5405 0003  et/flag.pngUT...
0000a790: 8d78 1264 7578 0b00 0104 0000 0000 0400  .x.dux..........
0000a7a0: 0000 0050 4b05 0600 0000 0002 0002 00a2  ...PK...........
0000a7b0: 0000 00c6 0b00 0000 00                   .........
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ binwalk -e flag.png 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2876, uncompressed size: 3029, name: secret/flag.png

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented

                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ dd if=flag.png of=hidden.zip bs=1 skip=39739
3198+0 records in
3198+0 records out
3198 bytes (3.2 kB, 3.1 KiB) copied, 0.00381916 s, 837 kB/s
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ unzip hidden.zip 
Archive:  hidden.zip
   creating: secret/
  inflating: secret/flag.png         
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ open secret/flag.png 

```
picoCTF{Hiddinng_An_imag3_within_@n_ima9e_d55982e8}
## Notas
## Referencias
