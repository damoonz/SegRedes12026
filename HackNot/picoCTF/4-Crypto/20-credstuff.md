## Descripción 
We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it? Download the leak [here](https://artifacts.picoctf.net/c/151/leak.tar). The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.
## Solución 
Se proporciona un `leak.tar` con `usernames.txt` y `passwords.txt` alineados línea por línea. El usuario `cultiris` está en la línea 378. La contraseña correspondiente es `cvpbPGS{P7e1S_54I35_71Z3}`, que es la flag codificada en ROT13.
```
echo "cvpbPGS{P7e1S_54I35_71Z3}" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
picoCTF{C7r1F_54V35_71M3}
## Notas
## Referencias