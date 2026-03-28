## Descripción 
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/9/flag2of2-final.pdf).
## Solución 
Es un pdf y una imagen al mismo tiempo, al cambiar la extensión por png se obtiene la bandera a la mitad, para la segunda parte es lo siguiente
```
┌──(moonz㉿damoonz)-[~/Documentos/picoctf]
└─$ binwalk -e fla2of2.png       

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
1149          0x47D           Zlib compressed data, default compression

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented

                                                                                               
┌──(moonz㉿damoonz)-[~/Documentos/picoctf]
└─$ cd _fla2of2.png.extracted   
                                                                                               
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/_fla2of2.png.extracted]
└─$ ls
47D  47D.zlib
                                                                                               
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/_fla2of2.png.extracted]
└─$ cat 47D                     
q 0.1 0 0 0.1 0 0 cm
0 g
q
10 0 0 10 0 0 cm BT
/R7 16 Tf
1 0 0 1 50 250 Tm
(1n_pn9_&_pdf_7f9bccd1})Tj
ET
Q
Q



```
picoCTF{f1u3n7_1n_pn9_&_pdf_7f9bccd1}
## Notas
## Referencias
