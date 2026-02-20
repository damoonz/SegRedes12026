## Descripción 
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/71/challenge.zip)
## Solución 
```
damoonz-picoctf@webshell:~$ cd drop-in/
damoonz-picoctf@webshell:~/drop-in$ ls -la
total 12
drwxr-xr-x 3 damoonz-picoctf damoonz-picoctf   45 Mar  9  2024 .
drwxr-xr-x 5 damoonz-picoctf damoonz-picoctf 4096 Feb 20 02:18 ..
drwxr-xr-x 8 damoonz-picoctf damoonz-picoctf 4096 Mar  9  2024 .git
-rw-r--r-- 1 damoonz-picoctf damoonz-picoctf   30 Mar  9  2024 flag.py
damoonz-picoctf@webshell:~/drop-in$ python flag.py
Printing the flag...
damoonz-picoctf@webshell:~/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
damoonz-picoctf@webshell:~/drop-in$ python flag.py
Printing the flag...
picoCTF{t3@mw0rk_damoonz-picoctf@webshell:~/drop-in$               
damoonz-picoctf@webshell:~/drop-in$ python flag.py
Printing the flag...
picoCTF{t3@mw0rk_damoonz-picoctf@webshell:~/drop-in$ git checkout feature/part-1 && cat flag.py && git checkout feat flag.py && git checkout feature/part-3&& cat flag.py
Already on 'feature/part-1'
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')Switched to branch 'feature/part-2'
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')Switched to branch 'feature/part-3'
print("Printing the flag...")

print("w0rk_4c24302f}")


```
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_4c24302f}
## Notas
El comando largo cambia entre ramas de git y muestra el archivo indicado en cada una, `$$` ejecuta el siguiente comando solo si el pasado funcionó

## Referencias