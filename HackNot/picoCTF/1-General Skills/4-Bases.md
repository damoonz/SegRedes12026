# Bases
## Descripción
What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.

## Solución
### Solución 1 -consola
```
damoonz-picoctf@webshell:~$ echo 'bDNhcm5fdGgzX3IwcDM1' | base64 -d
l3arn_th3_r0p35damoonz-picoctf@webshell:~$ 
```
picoCTF{l3arn_th3_r0p35}

### Solución 2 -Cyberchef
https://gchq.github.io/CyberChef/#recipe=From_Decimal('Space',false/disabled)To_Binary('Space',8/disabled)From_Hex('None'/disabled)From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YkROaGNtNWZkR2d6WDNJd2NETTE&ieol=CRLF&oeol=CRLF
### Solución 3 -Python

```
damoonz-picoctf@webshell:~$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import base64
>>> base64.b64decode('bDNhcm5fdGgzX3IwcDM1')
b'l3arn_th3_r0p35'
```

## Notas
## Referencias