#### Description

Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/c28a959c5605d5f67480d5dd3a77f302/cat.jpg)

Detalles: en el desafio se nos proporciona una imagen llamada "cat.jpg", que podemos descargar, tras descargarla, podemos ejecutar los comandos `file, hexdump and binwak`para verificar que sea una imagen jpg. Así que el archivo parece ser un archivo jpg válido. Al trabajar con imágenes, siempre es recomendable abrirlo y revisar sus metadatos para buscar autores, propiedades y otros datos interesantes. Solo necesitamos abrir la imagen con un visor de imágenes

Una forma más rápida de decodificar la cadena es `echo`copiar el texto y canalizarlo a `base64 -d`, de la siguiente manera:

echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 -d 


picoCTF{the_m3tadata_1s_modified}