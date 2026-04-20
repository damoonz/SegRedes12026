## Descripción 

In RSA, a small e value can be problematic, but what about N? Can you decrypt this? [values](https://challenge-files.picoctf.net/c_wily_courier/278a798f2fc4d2f3945588f28acb6f9a629b3eb05179b526e1de1bd3125b3c1b/values)
## Solución 
Se consideran los valores del archivo, se factoriza la n y los dos factores se consideran p y q, se aplican las fórmulas correspondientes
```
c= 15341890103764929939105506004034128738090325640037083301857608662849501626260517

n= 948406957756830799684818171639547165784816468744946013083947881743680617123566349

e= 65537

  

p= 1891771437429478964908181306574287207137

q= 501332739776173570344039681219489434626477

tn = (p-1)*(q-1)

d = pow(e, -1, tn)

m = pow(c,d,n)

  

print(f'm = {m}')

  

flag=bytes.fromhex('0'+ hex(m)[2:]).decode()

print(f'Flag = {flag}')


```
picoCTF{sma11_N_n0_g0od_1dc7ae91}
## Notas
## Referencias