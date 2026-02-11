# Wave a flag

## Descripción
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...
## Solución
```
damoonz-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/5a478d0b24d6a4f4185e3adb7a78c41cdad626fb02fe80e083dc33bf8b197d3d/warm
--2026-02-11 14:16:59--  https://challenge-files.picoctf.net/c_wily_courier/5a478d0b24d6a4f4185e3adb7a78c41cdad626fb02fe80e083dc33bf8b197d3d/warm
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.18, 3.160.5.40, 3.160.5.64, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19312 (19K) [application/octet-stream]
Saving to: 'warm'

warm                        100%[===========================================>]  18.86K  --.-KB/s    in 0.007s  

2026-02-11 14:16:59 (2.72 MB/s) - 'warm' saved [19312/19312]

damoonz-picoctf@webshell:~$ chmod +x warm
damoonz-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
damoonz-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
```



picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
## Notas
chmod +x da permisos de ejecución
## Referencias

