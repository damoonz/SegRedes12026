## Descripción 
Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

Additional details will be available after launching your challenge instance.
## Solución 
```
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ gzip disk.img.gz       
gzip: disk.img.gz already has .gz suffix -- unchanged
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ gunzip disk.img.gz     
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ ls
disk.img
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ mmls disk.img                                   
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ fls -o 2048 disk.img           
d/d 11: lost+found
r/r 12: ldlinux.sys
r/r 13: ldlinux.c32
r/r 15: config-virt
r/r 16: vmlinuz-virt
r/r 17: initramfs-virt
l/l 18: boot
r/r 20: libutil.c32
r/r 19: extlinux.conf
r/r 21: libcom32.c32
r/r 22: mboot.c32
r/r 23: menu.c32
r/r 14: System.map-virt
r/r 24: vesamenu.c32
V/V 25585:      $OrphanFiles
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ fls -o 206848 disk.img 470
r/r 2344:       .ash_history
d/d 3916:       .ssh
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ icat -o 206848 disk.img 2345                    
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLAAAAJgxpYKDMaWC
gwAAAAtzc2gtZWQyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLA
AAAECItu0F8DIjWxTp+KeMDvX1lQwYtUvP2SfSVOfMOChxYGCtd7hso2E7OQItY6aTjMMy
KZb1FVmeBfnVjyHcGYosAAAADnJvb3RAbG9jYWxob3N0AQIDBAUGBw==
-----END OPENSSH PRIVATE KEY-----
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ icat -o 206848 disk.img 2346
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIGCtd7hso2E7OQItY6aTjMMyKZb1FVmeBfnVjyHcGYos root@localhost
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ icat -o 206848 disk.img 2345 > id_ed25519
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ ls
disk.img  id_ed25519
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ ls -l id_ed25519 
-rw-rw-r-- 1 moonz moonz 411 mar 23 09:55 id_ed25519
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ chmod 600 id_ed25519 
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ ls -al          
total 235532
drwxrwxr-x 2 moonz moonz      4096 mar 23 09:55 .
drwxrwxr-x 3 moonz moonz      4096 mar  9 08:21 ..
-rw-rw-r-- 1 moonz moonz 241172480 ago  4  2023 disk.img
-rw------- 1 moonz moonz       411 mar 23 09:55 id_ed25519
                                                                             
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/forensic]
└─$ ssh -i id_ed25519 -p 54681 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:54681 ([13.59.203.175]:54681)' can't be established.
ED25519 key fingerprint is: SHA256:XBSvB1lk28EctsAVdKJtsl0A7C5bonqPrvHCYH8aEy4
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:5: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:54681' (ED25519) to the list of known hosts.
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.8.0-1047-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ cat flag.txt
picoCTF{k3y_5l3u7h_339601ed}ctf-player@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed


```
picoCTF{k3y_5l3u7h_339601ed}
## Notas
## Referencias