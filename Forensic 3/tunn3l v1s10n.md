
Description
We found this file. Recover the flag.

Detalles: Dado que el archivo descargable llamado "tunn3lv1s1on" es de un tipo desconocido, ejecutamos exiftool para determinar que es una imagen de mapa de bits la imagen no se visualiza correctamente al abrirla, por lo que podemos suponer que debe estar dañada. 
Para esto usamos 
exiftool tunn3l_v1s10n luego revisamos los bytes hexadecimales de la imagen y los modificamos para intentar repararla podemos usar un editor hexadecimal para luego 
cambiar "ba d0" del encabezado DIB a "28 00" y "32 01" del número de bits por píxel a "40 03" funciona y obtenemos la imagen correcta. Al renombrar el archivo "tunn3lv1s10n" a "tunn3lv1s10n.bmp", podemos abrirlo y obtener la bandera.


picoCTF{qu1t3_a_v13w_2020}

