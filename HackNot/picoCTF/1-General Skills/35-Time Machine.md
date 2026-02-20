# Time Machine
## Descripción 
What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/161/challenge.zip)
## Solución 
```
damoonz-picoctf@webshell:~/drop-in$ cd drop-in/
damoonz-picoctf@webshell:~/drop-in/drop-in$ cd ..
damoonz-picoctf@webshell:~/drop-in$ ls
drop-in
damoonz-picoctf@webshell:~/drop-in$ cd drop-in/
damoonz-picoctf@webshell:~/drop-in/drop-in$ ls -a
.  ..  .git  message.txt
damoonz-picoctf@webshell:~/drop-in/drop-in$ git log

[3]+  Stopped                 git log
damoonz-picoctf@webshell:~/drop-in/drop-in$ git checkout 10228f3d6437701ef5aaac04213757031f30ebec
Note: switching to '10228f3d6437701ef5aaac04213757031f30ebec'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 10228f3 picoCTF{t1m3m@ch1n3_8defe16a}


```
picoCTF{t1m3m@ch1n3_8defe16a}
## Notas
Se descarga el zip y se ve el historial de commits igual que el 34.


rm -rf *
		 borra todo lo de la carpeta actual, tmb directorios

## Referencias
