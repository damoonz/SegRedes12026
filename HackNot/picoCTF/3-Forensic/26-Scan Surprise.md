## Descripción 
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead? You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/16/challenge.zip)

The same files are accessible via SSH here: `ssh -p 64697 ctf-player@atlas.picoctf.net` Using the password `6abf4a82`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!
## Solución 
```
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ ssh -p64697 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:64697 ([18.217.83.136]:64697)' can't be established.
ED25519 key fingerprint is: SHA256:hVmbk/OaNT4902bBr7h26wfhmBuJWi4tub8AJqoAJCM
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:64697' (ED25519) to the list of known hosts.
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@atlas.picoctf.net's password: 
Permission denied, please try again.
ctf-player@atlas.picoctf.net's password:                 
ctf-player@challenge:~/drop-in$ ls -lah
total 4.0K
drwxr-xr-x 2 ctf-player ctf-player  22 Mar 12  2024 .
drwxr-xr-x 1 ctf-player ctf-player  20 Mar 26 15:49 ..
-rw-r--r-- 1 root       root       346 Mar 12  2024 flag.png
ctf-player@challenge:~/drop-in$ zbarimg flag.png 
Connection Error (Failed to connect to socket /var/run/dbus/system_bus_socket: No such file or directory)
Connection Null
QR-Code:picoCTF{p33k_@_b00_7843f77c}
scanned 1 barcode symbols from 1 images in 0.01 seconds

ctf-player@challenge:~/drop-in$ Connection to atlas.picoctf.net closed by remote host.
Connection to atlas.picoctf.net closed.



```
picoCTF{p33k_@_b00_7843f77c}
## Notas
## Referencias
