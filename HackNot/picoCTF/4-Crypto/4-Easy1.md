## Descripción 
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help UFJKXQZQUNB with the key of SOLVECRYPTO. Can you use this [table](https://challenge-files.picoctf.net/c_fickle_tempest/859ffc313a4d8b63149f144745043a7312fc4f993e405eeeb8ee5ae6ca8444a8/table.txt) to solve it?.
## Solución 
Se usa un cifrado vigenere, se utiliza el siguiente código para obtener la bandera
```
cipher = "UFJKXQZQUNB"

key = "SOLVECRYPTO"

flag = ""

  

for i in range(len(cipher)):

    # (C - K) mod 26

    dec = (ord(cipher[i]) - ord(key[i])) % 26

    flag += chr(dec + ord('A'))

  

print(f"picoCTF{{{flag}}}")


```
picoCTF{CRYPTOISFUN}
## Notas
## Referencias