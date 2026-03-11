## Descripción 
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.picoctf.net/c_fickle_tempest/bdd421d396847b0b8c86a2bc0c86331a18e2f9191b961b162f7c6379a4ca94be/whitepages.txt) is all blank!

## Solución 
Verificamos que el archivo es UTF-8 con lineas largas,
```
file whitepages.txt
```

Visualizamos el hexdump del archivo y vemos que es una seuencia de caracteres unicode (e2 80 83  y 20 )
```
xxd -g 1 -l 100 whitepages.txt
```

Reemplazamos e2 80 83  por 0s y 20 por 1s,
```
sed 's/\xe2\x80\x83/0/g' whitepages.txt | sed 's/\x20/1/g'
```

Convertimos del binario y sale la bandera
picoCTF{not_all_spaces_are_created_equal_aa90f80c1cebc20be3564d2f96a9726c}
## Notas
## Referencias