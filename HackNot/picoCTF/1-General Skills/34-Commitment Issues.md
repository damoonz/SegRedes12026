# Commitment Issues
## Descripción
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/76/challenge.zip)

## Solución 

```
damoonz-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/76/challenge.zip
--2026-02-20 01:35:53--  https://artifacts.picoctf.net/c_titan/76/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19201 (19K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                100%[=============================================>]  18.75K  --.-KB/s    in 0.008s  

2026-02-20 01:35:53 (2.42 MB/s) - 'challenge.zip' saved [19201/19201]

damoonz-picoctf@webshell:~$ unzip challenge.zip 
damoonz-picoctf@webshell:~$ cd drop-in/
damoonz-picoctf@webshell:~/drop-in$ ls -a
.  ..  .git  message.txt
damoonz-picoctf@webshell:~/drop-in$ git log

[1]+  Stopped                 git log
damoonz-picoctf@webshell:~/drop-in$ git checkout e720dc26a1a55405fbdf4d338d465335c439fb3e
Note: switching to 'e720dc26a1a55405fbdf4d338d465335c439fb3e'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at e720dc2 create flag
damoonz-picoctf@webshell:~/drop-in$ git log

[2]+  Stopped                 git log
damoonz-picoctf@webshell:~/drop-in$ git checkout e720dc26a1a55405fbdf4d338d465335c439fb3e
HEAD is now at e720dc2 create flag
damoonz-picoctf@webshell:~/drop-in$ cat message.txt 
picoCTF{s@n1t1z3_7246792d}
damoonz-picoctf@webshell:~$ cd drop-in/
damoonz-picoctf@webshell:~/drop-in$ ls -a
.  ..  .git  message.txt
damoonz-picoctf@webshell:~/drop-in$ git log

[1]+  Stopped                 git log
damoonz-picoctf@webshell:~/drop-in$ git checkout e720dc26a1a55405fbdf4d338d465335c439fb3e
Note: switching to 'e720dc26a1a55405fbdf4d338d465335c439fb3e'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at e720dc2 create flag
damoonz-picoctf@webshell:~/drop-in$ git log

[2]+  Stopped                 git log
damoonz-picoctf@webshell:~/drop-in$ git checkout e720dc26a1a55405fbdf4d338d465335c439fb3e
HEAD is now at e720dc2 create flag
damoonz-picoctf@webshell:~/drop-in$ cat message.txt 
picoCTF{s@n1t1z3_7246792d}
```
picoCTF{s@n1t1z3_7246792d}
## Notas

Ejecutar cd drop-in/ y con ls -a se puede ver el archivo ".git". El comando git log ve confirmaciones anteriores, y una de ellas tiene una nota que dice "create flag" con id largo

git checkout 3d5ec8a26ee7b092a1760fea18f384c35e435139
		 accede a confirmaciones anteriores


y con cat message.txt sale la flag
## Referencias