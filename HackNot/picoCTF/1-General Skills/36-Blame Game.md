## Descripción 

Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/72/challenge.zip)
## Solución 
```
damoonz-picoctf@webshell:~$ cd drop-in/
damoonz-picoctf@webshell:~/drop-in$ ls -a
.  ..  .git  message.py
damoonz-picoctf@webshell:~/drop-in$ git log


damoonz-picoctf@webshell:~/drop-in$ git log message.py

```
picoCTF{@sk_th3_1nt3rn_b64c4705}
## Notas

parecido al anterior, solo que message.py no estuvo en commit, pero especificando el archivo se puede ver el commit de la persona que hace que no pueda funcionar
## Referencias