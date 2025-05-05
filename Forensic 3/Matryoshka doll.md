

Description
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: this
El desafío nos da un enlace para descargar una imagen llamada dolls.jpg. Tomando como referencia el nombre del desafío, "Muñeca Matrioshka", podemos suponer que contiene archivos ocultos. Para extraerlos, usamos binwalk.

binwalk dolls.jpg
extraemos los archivos ocultos 
binwalk -e dolls.jpg
cd dolls.jpg.extracted/base_images
binwalk -e 2_c.jpg
cd 2_c.jpg.extracted/base_images
binwalk -e 3_c.jpg
cd _3_c.jpg.extracted/base_images
binwalk -e 4_c.jpg
cd _4_c.jpg.extracted
y para encontrar la bandera 
cat flag.txt 


picoCTF{336cf6d51c9d9774fd37196c1d7320ff}

