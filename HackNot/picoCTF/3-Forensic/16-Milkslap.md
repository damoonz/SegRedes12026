## Descripción 
🥛http://wily-courier.picoctf.net:57813/
## Solución 
En la hoja de estilos del url se ve que se carga una imagen, se toma el nombre de la imagen y se pone en el url, se descarga y se aumenta el stack con el siguiente comando, donde sale la bandera

```
──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ RUBY_THREAD_VM_STACK_SIZE=5242880 zsteg -a milkslap.png
imagedata           .. text: "\n\n\n\n\n\n\t\t"
chunk:0:IHDR        .. file: Adobe Photoshop Color swatch, version 0, 1280 colors; 1st RGB space (0), w 0xb9a0, x 0x802, y 0, z 0; 2nd HSB space (1), w 0, x 0, y 0, z 0                                                               
b1,b,lsb,xy         .. text: "picoCTF{imag3_m4n1pul4t10n_sl4p5}\n"
b1,bgr,lsb,xy       .. <wbStego size=0x941a5b ext=nil data="\xB6\xA


```
picoCTF{imag3_m4n1pul4t10n_sl4p5}
## Notas
## Referencias

