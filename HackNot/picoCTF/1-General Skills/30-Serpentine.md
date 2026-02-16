# Serpentine

## Descripción
Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/35/serpentine.py)
## Solución

```
damoonz-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/35/serpentine.py
--2026-02-16 15:07:01--  https://artifacts.picoctf.net/c/35/serpentine.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2550 (2.5K) [application/octet-stream]
Saving to: 'serpentine.py'

serpentine.py                100%[=============================================>]   2.49K  --.-KB/s    in 0s      

2026-02-16 15:07:01 (1.73 GB/s) - 'serpentine.py' saved [2550/2550]

damoonz-picoctf@webshell:~$ nano serpentine.py 
damoonz-picoctf@webshell:~$ python serpentine.py
What would you like to do? (a/b/c) c
damoonz-picoctf@webshell:~$ nano serpentine.py 
damoonz-picoctf@webshell:~$ python serpentine.py 

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}

Oops! I must have misplaced the print_flag function! Check my source code!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) c
```
picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
## Notas
Solo se agrego un print llamando la función que imprime la bandera
## Referencias