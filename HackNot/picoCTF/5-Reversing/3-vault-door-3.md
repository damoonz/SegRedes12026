## Descripción 
This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://challenge-files.picoctf.net/c_fickle_tempest/4cff24ee8b551078be8c14758fae20ab4a2dca78746aef367bc854491b8ee465/VaultDoor3.java)
## Solución 
Invertir cada bucle para encontrar la posición original de cada carácter:

    Bucle 1 (i=0-7): Directo → password[0-7] = "jU5t_a_s"

    Bucle 2 (i=8-15): password[23-i] = buffer[i] → Obtuve "1mpl3_an"

    Bucle 3 (i=16-30 paso 2): password[46-i] = buffer[i] → Obtuve posiciones pares restantes

    Bucle 4 (i=31-17 paso -2): password[i] = buffer[i] → Obtuve posiciones impares

Ensamblar todo en orden (posición 0 a 31) y obtener contraseña original.

picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_e60bc2}
## Notas
## Referencias