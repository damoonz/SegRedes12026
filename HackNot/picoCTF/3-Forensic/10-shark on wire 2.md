## Descripción 
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/f208f7c58d3703ed5fe0a78f707f011fcbb8c0b210b35247762c7ccacb49fe46/capture.pcap). Recover the flag.
## Solución 
Con scapy en python, primero instalamos scapy,
```
sudo apt install python3-scapy 
```

luego programamos el exploit que nos de la flag,

```
from scapy.all import *
packets = rdpcap('capture.pcap')
flag=''
for p in packets:
    if UDP in p and p[UDP].dport == 22:
        if p[UDP].sport > 5000:
            flag+=chr(p[UDP].sport - 5000)

print(flag)
```
picoCTF{p1llf3r3d_data_v1a_st3g0}
## Notas
## Referencias