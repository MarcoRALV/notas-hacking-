#### Description

We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag. 



Detalles: descargamos el archivo del reto lo pegamos en nuestra terminal de la siguiente forma 
wget https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery
vamos con el comando 
file mystery
y lo editamos con hexeditor 
ponemos el comando 
pngcheck -v mystery, vemos que no tiene errores y abrimos el archivo con 
open mystery y ahi estara la bandera 

picoCTF{c0rrupt10n_1847995}


Apoyo: https://www.youtube.com/watch?v=7zY4VkiWbBI&ab_channel=hackadvisermx