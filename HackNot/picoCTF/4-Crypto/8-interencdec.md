## Descripción 
Can you get the real meaning from this file. Download the file [here](https://artifacts.picoctf.net/c_titan/111/enc_flag).
## Solución 
Decodificar base64,
Eliminar caracteres : 'b y ',
Decodificar nuevamente en base64,
```
cat enc_flag | base64 -d | tr -d "'b" | base64 -d
```

Ir a cyberchef elegir la receta rot13 y rotar 19 posiciones


picoCTF{caesar_d3cr9pt3d_890d2379}
## Notas
## Referencias