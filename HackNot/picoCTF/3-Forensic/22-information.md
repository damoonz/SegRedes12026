## Descripción 
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg)
## Solución 
Viendo los metadatos del archivo se ve que la parte de licencia tiene un string raro para ser una licencia,  se puede considerar un string encriptado en base 64, con un comando en la terminal se puede desencriptar y justamente luego se da la bandera
```
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 -d
picoCTF{the_m3tadata_1s_modified}                                                                             
```

picoCTF{the_m3tadata_1s_modified}
## Notas
## Referencias