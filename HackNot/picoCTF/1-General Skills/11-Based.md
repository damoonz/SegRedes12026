# Based
## Descripción
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?

Additional details will be available after launching your challenge instance.

## Solución
```
damoonz-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 50686
Let us see how data is stored
pear
Please give the 01110000 01100101 01100001 01110010 as a word.
...
you have 45 seconds.....

Input:
pear
Please give me the  o163 o164 o162 o145 o145 o164 as a word.
Input:
street
Please give me the 66616c636f6e as a word.
Input:
falcon
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_acdCcfCa}
```

https://gchq.github.io/CyberChef/#input=MDExMTAwMDAgMDExMDAxMDEgMDExMDAwMDEgMDExMTAwMTA

https://gchq.github.io/CyberChef/#recipe=Find_/_Replace(%7B'option':'Regex','string':'o'%7D,'',true,false,true,false)From_Octal('Space')&input=bzE2MyBvMTY0IG8xNjIgbzE0NSBvMTQ1IG8xNjQ

https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=NjY2MTZjNjM2ZjZl

picoCTF{learning_about_converting_values_acdCcfCa}
## Notas
Octal -números del 0-7
## Referencias