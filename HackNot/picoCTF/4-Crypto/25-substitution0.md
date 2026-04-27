## Descripción 
A message has come in but it seems to be all scrambled. Luckily it seems to have the key at the beginning. Can you crack this substitution cipher? Download the message [here](https://artifacts.picoctf.net/c/154/message.txt).
## Solución 
El texto comienza con la cadena sospechosa `PAQZTNDSRYWFEXGJKCVLBUHOMI` (26 caracteres, uno por letra del alfabeto), que es el alfabeto de sustitución, se usa el siguiente código en python para obtener la bandera
```
# Clave dada (mapeo: A->Z, B->G, C->S, etc.)

key = "ZGSOCXPQUYHMILERVTBWNAFJDK"

  

# Crear mapeo inverso (cifrado -> claro)

cipher_to_plain = {}

alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"

  

for i in range(26):

cipher_to_plain[key[i]] = alphabet[i]

# También para minúsculas

cipher_to_plain_lower = {}

for i in range(26):

cipher_to_plain_lower[key[i].lower()] = alphabet[i].lower()

  

# Mensaje cifrado

ciphertext = """Qctcnrel Mcptzlo ztebc, fuwq z ptzac zlo bwzwcmd zut, zlo gtenpqw ic wqc gccwmc

xtei z pmzbb szbc ul fqusq uw fzb clsmebco. Uw fzb z gcznwuxnm bsztzgzcnb, zlo, zw

wqzw wuic, nlhlefl we lzwntzmubwb—ex sentbc z ptczw rtukc ul z bsuclwuxus reulw

ex aucf. Wqctc fctc wfe tenlo gmzsh brewb lczt elc cjwtciuwd ex wqc gzsh, zlo z

melp elc lczt wqc ewqct. Wqc bszmcb fctc cjsccoulpmd qzto zlo pmebbd, fuwq zmm wqc

zrrcztzlsc ex gntlubqco pemo. Wqc fcupqw ex wqc ulbcsw fzb actd tcizthzgmc, zlo,

wzhulp zmm wqulpb ulwe selbuoctzwuel, U senmo qztomd gmzic Ynruwct xet qub eruluel

tcbrcswulp uw.

  

Wqc xmzp ub: ruseSWX{5NG5717N710L_3A0MN710L_357GX9XX}"""

  

# Decodificar

decoded = []

for ch in ciphertext:

if ch in cipher_to_plain:

decoded.append(cipher_to_plain[ch])

elif ch in cipher_to_plain_lower:

decoded.append(cipher_to_plain_lower[ch])

else:

decoded.append(ch)

  

print(''.join(decoded))


```
picoCTF{5UB5717U710N_3V0LU710N_357BF9FF}
## Notas
## Referencias