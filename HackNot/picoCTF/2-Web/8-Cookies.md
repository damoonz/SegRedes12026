## Descripción 
Who doesn't love cookies? Try to figure out the best one.http://wily-courier.picoctf.net:58156/
## Solución 
```

┌──(moonz㉿damoonz)-[~]
└─$ for i in {1..30}; do curl -s http://wily-courier.picoctf.net:56497/check -H "Cookie: name=$i"; done | grep pico 
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}


```

picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}

## Notas
## Referencias