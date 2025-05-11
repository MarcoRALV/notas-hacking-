#### Description

Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/259/flag.png).

detalles: descargamos el reto 
marcorojas@MarcoRojas:~$ wget https://artifacts.picoctf.net/c/259/flag.png
--2025-05-11 14:13:05--  https://artifacts.picoctf.net/c/259/flag.png
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.61, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 42930 (42K) [application/octet-stream]
Saving to: ‘flag.png’

flag.png                      100%[=================================================>]  41.92K  --.-KB/s    in 0.05s

2025-05-11 14:13:05 (854 KB/s) - ‘flag.png’ saved [42930/42930] 
y vamos con 
marcorojas@MarcoRojas:~$ binwalk flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2869, uncompressed size: 3024, name: secret/flag.png
42908         0xA79C          End of Zip archive, footer length: 22

marcorojas@MarcoRojas:~$ binwalk -e flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2869, uncompressed size: 3024, name: secret/flag.png
42908         0xA79C          End of Zip archive, footer length: 22



marcorojas@MarcoRojas:~$ cd _flag.png.extracted
marcorojas@MarcoRojas:~/_flag.png.extracted$ ls
29  29.zlib  9B3B.zip  secret
marcorojas@MarcoRojas:~/_flag.png.extracted$ cd secret/
marcorojas@MarcoRojas:~/_flag.png.extracted/secret$ ls
flag.png
marcorojas@MarcoRojas:~/_flag.png.extracted/secret$ ls -al
total 12
drwxr-xr-x 2 marcorojas marcorojas 4096 Mar 15  2023 .
drwxr-xr-x 3 marcorojas marcorojas 4096 May 11 14:14 ..
-rw-r--r-- 1 marcorojas marcorojas 3024 Mar 15  2023 flag.png
marcorojas@MarcoRojas:~/_flag.png.extracted/secret$ eog flag.png
y veremos esta imagen 
![[Pasted image 20250511141928.png]]

picoCTF{Hiddinng_An_imag3_within_@n_ima9e_cda72af0}