## Descripción 
What happens if you have a small exponent? There is a twist though, we padded the plaintext so that (M ** e) is just barely larger than N. Let's decrypt this: [values](https://challenge-files.picoctf.net/c_wily_courier/516811e1405ca0cb6f6a464fb3da27ea64fb10819c2e8060cf9d9c5f79612fc8/values)

## Solución 

- Como tu exponente e es 3 (muy pequeño), la vulnerabilidad es un ataque de raíz cúbica conocido como: Stereotyped attack o small e attack.
- Este ataque funciona si el mensaje original m fue lo suficientemente pequeño como para que:
    m^3 < n. 
- Si eso ocurrió, el módulo no tuvo efecto, y por lo tanto c = m^3
    c = m ^ e mod n
    c = m ^ 3
- Para revertirlo, solo necesitamos calcular la raíz cúbica de c.
    m = raiz3(c)
    
Se compila este código
```

import gmpy2

n = ...
e = ...
c = ... 

print("Calculando la raíz cúbica de c...")

m, es_exacta = gmpy2.iroot(c, 3)

if es_exacta:
    print("\n¡Raíz cúbica perfecta encontrada!")
    print(f"Mensaje (entero): {m}")
    flag = bytes.fromhex(hex(m)[2:]).decode()
    print(f"FLAG: {flag}")
else:
    print("\nNo se encontró una raíz cúbica perfecta.")
    print("Este ataque (small e) no funcionó.")
```

picoCTF{e_sh0u1d_b3_lArg3r_92f4d5a5}
## Notas
## Referencias