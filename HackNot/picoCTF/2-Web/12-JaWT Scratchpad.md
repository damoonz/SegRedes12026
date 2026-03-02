## Descripción 
Check the admin scratchpad!

Additional details will be available after launching your challenge instance.

## Solución 

- Nos logueamos con cualquier usuario
- Copiamos el token jwt a un archivo llamado token
- Lo crackeamos en kali usando john con el diccionario rockyou.txt
```
gizip -d /usr/share/wordlists/rockyou.txt.gz john token -w=/usr/share/wordlists/rockyou.txt
```
- vamos al sitio jwt debuger, y modificamos el payload por admin
- ponemos la palabra crackeada en la firma
- copiamos el nuevo token generado a la cookie y recargamos la pagina
picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}
## Notas
## Referencias