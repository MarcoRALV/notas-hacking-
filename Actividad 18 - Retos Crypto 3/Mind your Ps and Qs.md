

#### Description

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/38f30029ab93478310e906d3d084a4c1/values)

Detalles: descargamos el archivo que se nos proporciona, lo abrimos y vemos lo siguiente : 
Decrypt my super sick RSA:
c: 240986837130071017759137533082982207147971245672412893755780400885108149004760496
n: 831416828080417866340504968188990032810316193533653516022175784399720141076262857
e: 6553 
vamos a https://www.dcode.fr/rsa-cipher y remplazamos el valor de c y n y le damos clic en decodificar y nos dara la bandera

picoCTF{sma11_N_n0_g0od_23540368}


Fuente: https://www.youtube.com/watch?v=pdAHWr5cxRc&ab_channel=COZT 
