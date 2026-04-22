## Descripción 
How about we take you on an adventure on exploring certificate signing requests Take a look at this CSR file [here](https://artifacts.picoctf.net/c/425/readmycert.csr).
## Solución 
Leer un archivo con extension .csr en la consola y aparece la bandera
```
openssl req -in readmycert.csr -noout -text
```
picoCTF{read_mycert_693f7c03}
## Notas
## Referencias