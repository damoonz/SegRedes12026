## Descripción
Decrypt this message. Message: [message](https://challenge-files.picoctf.net/c_fickle_tempest/324327ef0dc439d37f8ea25706618c6a389672b2ce2bc56101d6ee6e24f98e15/data.enc)
## Solución 
El mensaje se encuentra en cifrado cesar, se resuelve por fuerza bruta utilizando este código
```
def brute_force_caeser_cipher(encrypted_flag):

 alphabet = "abcdefghijklmnopqrstuvwxyz"  # Define the alphabet - in this case is the latin alphabet

  

 length_text = len(encrypted_flag)

  

 for shift in range(26):

     decrypted_message = ""

     for char in encrypted_flag:

      if char in alphabet:

       new_char = chr(((ord(char) - 97 - shift) % 26) + 97) # Decrypt the character using modular arithmetic

       decrypted_message += new_char

      else:

       decrypted_message += char  # Keep non-alphabet characters unchanged

     print(f"Shift {shift}: {decrypted_message}")  # Print the result for this shift

  

brute_force_caeser_cipher("furvvlqjwkhuxelfrqslandktj")


```

En la tercer línea de la salida se muestra el contenido de la bandera
picoCTF{crossingtherubiconpixkahqg}
## Notas
## Referencias