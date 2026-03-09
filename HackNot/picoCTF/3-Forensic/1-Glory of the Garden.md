## Descripción 
This file contains more than it seems.Get the flag from [garden.jpg](https://challenge-files.picoctf.net/c_fickle_tempest/b67cf664cdf2557bea4f1d6079bc099037bc6ea5322afbfc80c5dcf4440c5e7d/garden.jpg).
## Solución 
Con editor hexadecimal se busca en la imagen la palabra clave del formato de la bandera:
```
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/gloryofthegarden]
└─$ hexeditor garden.jpg      
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/gloryofthegarden]
└─$ strings garden.jpg | grep pico
Here is a flag: picoCTF{more_than_m33ts_the_3y398ee229a}

```

picoCTF{more_than_m33ts_the_3y398ee229a}
## Notas
## Referencias
