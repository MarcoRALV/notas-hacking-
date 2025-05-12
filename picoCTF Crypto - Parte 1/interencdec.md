#### Description

Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/1/enc_flag).


Detalles: 
descargamos el reto 
marcorojas@MarcoRojas:~$ wget https://artifacts.picoctf.net/c_titan/1/enc_flag
--2025-05-11 17:37:48--  https://artifacts.picoctf.net/c_titan/1/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.64, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 73 [application/octet-stream]
Saving to: ‘enc_flag’

enc_flag                      100%[=================================================>]      73  --.-KB/s    in 0s

2025-05-11 17:37:48 (6.08 MB/s) - ‘enc_flag’ saved [73/73]


marcorojas@MarcoRojas:~$ ls enc_flag
enc_flag
marcorojas@MarcoRojas:~$ base64 -e enc_flag
base64: invalid option -- 'e'
Try 'base64 --help' for more information.
marcorojas@MarcoRojas:~$ base64 -d enc_flag
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ=='

nos encontramos con esta decodificacion en base64 
una ves que lo decodificamos obtendremos lo siguiente 
wpjvJAM{jhlzhy_k3jy9wa3k_lh60l00i} 
usamos https://www.dcode.fr/caesar-cipher
selecionamos rot13 y pegamos lo anterior y obtenemos asi nuestra bandera

picoCTF{caesar_d3cr9pt3d_ea60e00b}