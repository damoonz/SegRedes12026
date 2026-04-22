## Descripción
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://challenge-files.picoctf.net/c_wily_courier/3dced65f7a857f7a28f538da0f98fdceca989646f69d4651133b5c04590b0b0d/scrambled1.png) [scrambled2.png](https://challenge-files.picoctf.net/c_wily_courier/3dced65f7a857f7a28f538da0f98fdceca989646f69d4651133b5c04590b0b0d/scrambled2.png)

## Solución 
- Descargamos `stegsolve` :

`cd /opt sudo wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar sudo chmod +x stegsolve.jar java -jar /opt/stegsolve.jar` 

- Abrimos la primer imagen
    
    - `File - Open`
    
- La combinamos con la segunda
    
    - `Analyse - Image Combiner`
    
- Usamos los iconos de flecha en la parte de abajo para elegir el tipo de combinación hasta encontrar AND


picoCTF{8cdf93c3}
## Notas
## Referencias
