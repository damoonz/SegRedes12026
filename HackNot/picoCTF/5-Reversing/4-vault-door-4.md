## Descripción 
This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://challenge-files.picoctf.net/c_fickle_tempest/3af806b1d880a4a7cecd00831a8bcc913cf57c68cb7f5cfb8597f710c5d771e1/VaultDoor4.java)
## Solución 
Para obtener la contraseña, simplemente convertí cada valor del arreglo `myBytes` a su carácter ASCII correspondiente, ya que cada número representa un byte de la contraseña.

Los valores estaban en 4 formatos diferentes:

1. **Los primeros 8** eran decimales normales → los convertí directamente a caracteres
    
2. **Los siguientes 8** estaban en hexadecimal (prefijo `0x`) → los convertí a decimal y luego a carácter
    
3. **Los siguientes 8** estaban en octal (prefijo `0`) → los convertí a decimal y luego a carácter
    
4. **Los últimos 8** ya eran caracteres literales entre comillas simples
    

Al convertir cada uno y unirlos en orden, obtuve la contraseña:
picoCTF{jU5t_4_bUnCh_0f_bYt3s_13df618a23}
## Notas
## Referencias