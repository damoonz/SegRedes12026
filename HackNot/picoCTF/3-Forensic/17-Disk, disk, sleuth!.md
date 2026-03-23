## Descripción 
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image.[dds1-alpine.flag.img.gz](https://challenge-files.picoctf.net/c_wily_courier/27cbd6a2ed4a59d600f2a24c1ccaa6de66f9aeee95d6b365160fd75649e45f1b/dds1-alpine.flag.img.gz)
## Solución 

Extrae el disco ejecutando `gunzip dds1-alpine.flag.img.gz`.

Asegúrate de tener Autopsy instalado (`sudo apt install autopsy`).

Usa el comando `srch_strings` como se sugiere en el desafío y luego busca picoCTF: `srch_strings dds1-alpine.flag.img | grep picoCTF`.


picoCTF{f0r3ns1c4t0r_n30phyt3_5e56e786}
## Notas
## Referencias