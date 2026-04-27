## Descripción 
We received an encrypted message. The modulus is built from primes large enough that factoring them isn’t an option, at least not today. See if you can make sense of the numbers and reveal the flag.Download the [message](https://challenge-files.picoctf.net/c_amiable_citadel/064d4179839d2d7423ffdb19ce407b8ab56ac27afbb579983a98ced35a174ea4/message.txt).
## Solución
Nos dan un mensaje cifrado con RSA. No se puede factorizar n, e tiene un valor muy pequeño, al elevarlo a 20 el resultado puede ser menor que n. Este script en Python busca la raíz entera 20 usando búsqueda binaria. Si no la encuentra, prueba con k = 1, 2, 3...
```

def integer_nth_root(num, n):
    low, high = 1, 1
    while high ** n <= num:
        high *= 2
    while low <= high:
        mid = (low + high) // 2
        if mid ** n == num:
            return mid
        elif mid ** n < num:
            low = mid + 1
        else:
            high = mid - 1
    return None

e = 20
m = integer_nth_root(c, e)

if m:
    flag = bytes.fromhex(hex(m)[2:]).decode()
else:
    for k in range(1, 10000):
        cand = c + k * n
        m = integer_nth_root(cand, e)
        if m:
            flag = bytes.fromhex(hex(m)[2:]).decode()
            break

print(flag)

```

picoCTF{t1ny_e_4da5fb4d}

## Notas
## Referencias