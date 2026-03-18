## Descripción 
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one?
Image: dolls.jpg

## Solución 
Tenemos imágenes dentro de otras imágenes, se descomprimen las imágenes y nos metemos a la carpeta indicada hasta que salga la bandera.
```
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ binwalk dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378933, uncompressed size: 383920, name: base_images/2_c.jpg
651591        0x9F147         End of Zip archive, footer length: 22

                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ unzip dolls.jpg 
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/2_c.jpg     
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ ls
base_images  dolls.jpg  Forensics_is_fun.pptm
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ cd base_images 
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic/base_images]
└─$ unzip dolls.jpg
unzip:  cannot find or open dolls.jpg, dolls.jpg.zip or dolls.jpg.ZIP.
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic/base_images]
└─$ ls
2_c.jpg
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic/base_images]
└─$ unzip 2_c.jpg  
Archive:  2_c.jpg
warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/3_c.jpg     
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic/base_images]
└─$ ls
2_c.jpg  base_images
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic/base_images]
└─$ unzip 2_c.jpg 
Archive:  2_c.jpg
warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile
  (attempting to process anyway)
replace base_images/3_c.jpg? [y]es, [n]o, [A]ll, [N]one, [r]ename: ^C                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic/base_images]
└─$ cd base_images

```
picoCTF{LL9lb1dR4QbGe4l4iWCvGq9pdtwt7392}

## Notas
## Referencias