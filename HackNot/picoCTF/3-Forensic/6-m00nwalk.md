## Descripción 
Decode this [message](https://challenge-files.picoctf.net/c_fickle_tempest/d372c5aa057b687f120292b30c70af827c64bd3661490e3e2f41551ff95394f0/message.wav) from the moon.
## Solución 
-Verificamos el tipo de archivo con file
```
file message.wav 
```

Descargamos decodificador STTV de github y lo instalamos,
```
https://github.com/colaclanth/sstv
cd /opt
sudo git clone https://github.com/colaclanth/sstv
cd sstv
https://github.com/colaclanth/sstv
```

Decodificamos el mensaje oculto en el .wav y lo guardamos en flag.png,
```
sstv -d message.wav -o flag.png
```

Abrimos el archivo y copiamos la flag de la imagen
```
open flag.png
```
picoCTF{beep_boop_im_in_space}
## Notas
## Referencias