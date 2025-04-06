
#### Description

The flag is somewhere on this web application not necessarily on the website. Find it.

Additional details will be available after launching your challenge instance.

Detalles : vamos al link que se nos proporciona http://saturn.picoctf.net:50471/ luego agregamos un /robots.txt al link
http://saturn.picoctf.net:50471/robots.txt, 
encontraremos lo siguiente 
ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg  
vamos a la pagina : https://www.base64decode.org/es/ y pegamos lo anterior nos saldra lo siguiente flag1.txtjs/myfif2זfRG@,z谖/u%z8 esto no nos sirve para nada entonces dejamos solo la linea de en medio 
anMvbXlmaWxlLnR4dA==
y obtendremos js/myfile.txt 
se lo agregamos al link inicial de la siguiente forma 
http://saturn.picoctf.net:50471/js/myfile.txt
y encontramos la bandera 
picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043} 



