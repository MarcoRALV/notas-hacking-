Description
I've hidden a flag in this file. Can you find it? Forensics is fun.pptm

Detalles: para solucionar este reto lo primero que tenemos que hacer es descargar el archivo del reto, una vez echo esto vemos que son archivos empaquetados, para des empaquetarlo usaremos unzip y lo renombramos 
mv WeakEdge.pptx WeakEdge.zip
unzip WeakEdge.zip -d extracted_ppt 
Buscamos en metadatos con 
exiftool WeakEdge.pptx | grep -i pico
Buscar en archivos XML
cd extracted_ppt
grep -r "picoCTF" .
cat ppt/comments/comment1.xml



picoCTF{D1d_u_kn0w_ppts_r_z1p5}


