## Descripción 
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/picopico.key). Recover the flag.
## Solución 
En el flujo salía una imagen, la descargamos y buscamos la bandera como string en la terminal
```
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ wireshark capture.pcap 
^C
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ strings vulture.jpg|grep pico                              
picoCTF{honey.roasted.peanuts}
                                       
```
picoCTF{honey.roasted.peanuts}

## Notas
## Referencias