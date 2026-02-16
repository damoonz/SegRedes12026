# PW Crack 3

## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Solución
```
damoonz-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/18/level3.py
damoonz-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
damoonz-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/18/level3.hash.bin
damoonz-picoctf@webshell:~$ echo "hola mundo" | md5sum
1e04bb3f9f396d3b71d93d326ebfc42d  -
damoonz-picoctf@webshell:~$ nano level3.              
level3.flag.txt.enc  level3.hash.bin      level3.py            
damoonz-picoctf@webshell:~$ nano level3.py
damoonz-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: 8799
That password is incorrect
damoonz-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: d3ab    
That password is incorrect
damoonz-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: 1ea2
That password is incorrect
damoonz-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: acaf
That password is incorrect
damoonz-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
```

picoCTF{m45h_fl1ng1ng_6f98a49f}
## Notas
Se tuvo que solucionar con un ciclo en el archivo .py para poder revisar todas las contraseñas
## Referencias
