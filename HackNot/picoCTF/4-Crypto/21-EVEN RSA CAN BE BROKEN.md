## Descripción
This service provides you an encrypted flag. Can you decrypt it with just N & e? Connect to the program with netcat: `$ nc verbal-sleep.picoctf.net 63978` The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_verbal_sleep/c798cbe85b3e431345406f393827b9b905481b5fcd6d4b4a845527ee0602da9b/encrypt.py).

## Solución 
Aunque `e` es seguro, los primos `p` y `q` probablemente fueron generados de forma débil (cercanos entre sí o con alguna otra falla).  
Esto hace que `N` sea factorizable. En lugar de atacar con Fermat (muy lento), usar directamente la base de datos factordb.com, donde ya estaban los factores.
```
# solve_no_crypto_fast.py

import json

import urllib.request

  

N = 13720904679529039460961675171090796233511849971338599435633264360402479754253092512095132358778116220337738661465554070372966733782607169213678071901570878

e = 65537

c = 9539727874811730679758322759065485914812389788952812302446391776953885065423347958868015196335969531745287345450898946863694211319039734650895895235720981

  

def int_to_text(num):

hex_str = hex(num)[2:]

if len(hex_str) % 2:

hex_str = '0' + hex_str

return bytes.fromhex(hex_str).decode('utf-8')

  

print("[*] Consultando factordb.com...")

url = f"http://factordb.com/api?query={N}"

with urllib.request.urlopen(url) as response:

data = json.loads(response.read().decode())

  

if 'factors' in data and len(data['factors']) >= 2:

p = int(data['factors'][0][0])

q = int(data['factors'][1][0])

print(f"[+] p = {p}")

print(f"[+] q = {q}")

phi = (p-1)*(q-1)

# Calcular inverso modular manualmente

def mod_inverse(a, m):

m0, x0, x1 = m, 0, 1

while a > 1:

q = a // m

a, m = m, a % m

x0, x1 = x1 - q * x0, x0

return x1 + m0 if x1 < 0 else x1

d = mod_inverse(e, phi)

m = pow(c, d, N)

flag = int_to_text(m)

print(f"\n🎉 Flag: {flag}")


```
picoCTF{tw0_1$_pr!m341c6ed35}
## Notas
## Referencias
