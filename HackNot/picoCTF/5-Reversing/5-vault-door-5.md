## Descripción 
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://challenge-files.picoctf.net/c_fickle_tempest/e0273648f1276c71952d98ee6611263932f766fd288de297c1881a0e4fcd775c/VaultDoor5.java)

## Solución 
Invertir el proceso de codificación: decodifiqué Base64 el string expected para obtener el URL encoding y decodifiqué URL encoding para obtener la contraseña original
```
import base64
from urllib.parse import unquote

expected = "JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVm" \
           "JTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2" \
           "JTM0JTVmJTM0JTMyJTYzJTM2JTM0JTMwJTM5JTYy"

# Decodificar Base64
url_encoded = base64.b64decode(expected).decode('utf-8')

# Decodificar URL encoding
password = unquote(url_encoded)

print(password)
```
picoCTF{c0nv3rt1ng_fr0m_ba5e_64_42c6409b}
## Notas
## Referencias