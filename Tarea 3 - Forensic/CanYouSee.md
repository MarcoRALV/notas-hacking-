#### Description

How about some hide and seek?Download this file [here](https://artifacts.picoctf.net/c_titan/6/unknown.zip). 

Detalles: para resolver este reto primero lo vamos a descargar 

marcorojas@MarcoRojas:~$ wget https://artifacts.picoctf.net/c_titan/6/unknown.zip
--2025-05-11 13:00:13--  https://artifacts.picoctf.net/c_titan/6/unknown.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.26, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2252298 (2.1M) [application/octet-stream]
Saving to: ‘unknown.zip’

unknown.zip                   100%[=================================================>]   2.15M  14.2MB/s    in 0.2s

2025-05-11 13:00:14 (14.2 MB/s) - ‘unknown.zip’ saved [2252298/2252298]


luego lo descomprimimos 
marcorojas@MarcoRojas:~$ unzip unknown.zip
Archive:  unknown.zip
  inflating: ukn_reality.jpg
marcorojas@MarcoRojas:~$ ls ukn_reality.jpg
ukn_reality.jpg
ponemos el siguiente comando 
marcorojas@MarcoRojas:~$ exiftool ukn_reality.jpg
y encontramos esta liena la cual decofificaremos en base64 para encontrar la bandera 
cGljb0NURntNRTc0RDQ3QV9ISUREM05fYTZkZjhkYjh9Cg 

picoCTF{ME74D47A_HIDD3N_a6df8db8}