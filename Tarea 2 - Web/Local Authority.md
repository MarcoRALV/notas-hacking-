
#### Description

Can you get the flag?

Additional details will be available after launching your challenge instance. 


Detalles: 
ir al sitio que se nos pone en el reto http://saturn.picoctf.net:53300/ dar clic derecho para inspeccionar el código fuente  
no encontraremos nada 
entonces lo que haremos sera agregar al link que se nos proporciona lo siguiente /login.php una ves echo esto damos clic derecho y nos vamos al código fuente y ahi encontraremos un script en java [secure.js](http://saturn.picoctf.net:53300/secure.js) si lo cliqueamos veremos que nos arrojara la contraseña y el pasword : 
username === 'admin' && password === 'strongPassword098765'
si los ponemos en la pagina inicial vamos a encontrar la bandera  picoCTF{j5_15_7r4n5p4r3n7_05df90c8}
