## Descripción 
How about some hide and seek?Download this file [here](https://artifacts.picoctf.net/c_titan/129/unknown.zip).
## Solución 
Se inspeccionan los metadatos de la imagen, en attribution url sale una cadena de base 64, se hace la conversión
```
┌──(moonz㉿damoonz)-[~/Documentos/picoctf]
└─$ exiftool -a -G1 -s -AttributionURL -AttributionName ukn_reality.jpg 
[XMP-cc]        AttributionURL                  : cGljb0NURntNRTc0RDQ3QV9ISUREM05fYjMyMDQwYjh9Cg==


```
picoCTF{ME74D47A_HIDD3N_b32040b8}

## Notas
## Referencias