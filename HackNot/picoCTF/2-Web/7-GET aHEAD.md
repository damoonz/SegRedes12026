## Descripción 
Find the flag being held on this server to get ahead of the competitionhttp://wily-courier.picoctf.net:64604/
## Solución 
```
                                                                             
┌──(moonz㉿damoonz)-[~]
└─$ curl -I  http://wily-courier.picoctf.net:64604/
HTTP/1.1 200 OK
Date: Wed, 25 Feb 2026 14:08:57 GMT
Server: Apache/2.4.38 (Debian)
X-Powered-By: PHP/7.2.34
flag: picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
Content-Type: text/html; charset=UTF-8



```
 picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
## Notas

curl -I  http://wily-courier.picoctf.net:64604/
	Pide encabezados
## Referencias