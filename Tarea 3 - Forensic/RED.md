#### Description

RED, RED, RED, REDDownload the image: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)


Al abrir el archivo de imagen, solo podemos ver lo siguiente. Sin embargo, sabiendo que **la esteganografía suele combinarse con la ciencia forense en una sola categoría,** decidí investigar la imagen a fondo utilizando herramientas esteganografías.
zsteg **analiza imágenes** para detectar **datos ocultos** (esteganografía). Además, es capaz de extraer información oculta del **bit menos significativo (LSB)** y otras **técnicas esteganográficas** .

Usando el webshell pico y el comando:

 zsteg -a rojo.png

Pude encontrar lo que parecía una cadena codificada en base64:
 “cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==”

Lo llevé a [CyberChef](https://gchq.github.io/CyberChef) para descifrarlo

picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}