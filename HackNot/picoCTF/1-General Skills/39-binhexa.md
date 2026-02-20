## Descripción 

How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 57042`
## Solución 
```
damoonz-picoctf@webshell:~$ nc titan.picoctf.net 57042

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 00000011
Binary Number 2: 01000110


Question 1/6:
Operation 1: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 00000110
Correct!

Question 2/6:
Operation 2: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 01001001
Correct!

Question 3/6:
Operation 3: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 00100011
Correct!

Question 4/6:
Operation 4: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00000010
Correct!

Question 5/6:
Operation 5: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 01000111
Correct!

Question 6/6:
Operation 6: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11010010
Correct!

Enter the results of the last operation in hexadecimal: D2

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d6f8047e}


```
picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d6f8047e}
## Notas
## Referencias