#### Description

I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/3/challenge.zip)

Additional details will be available after launching your challenge instance.


detalles: 
descargamos el reto 
marcorojas@MarcoRojas:~$ wget https://artifacts.picoctf.net/c_atlas/3/challenge.zip
--2025-05-11 13:42:34--  https://artifacts.picoctf.net/c_atlas/3/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.100, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 741 [application/octet-stream]
Saving to: ‘challenge.zip’

challenge.zip                 100%[=================================================>]     741  --.-KB/s    in 0s

2025-05-11 13:42:34 (66.5 MB/s) - ‘challenge.zip’ saved [741/741] 

y vamos con lo siguiente 

marcorojas@MarcoRojas:~$ ls
'Forensics is fun.pptm'     challenge.zip             disk.flag.img.gz.2   hash                    retos
'Forensics is fun.pptm.1'   cookies                   disk.img             heapdump                server.py
'Forensics is fun.pptm.2'   dds1-alpine.flag.img      flag.txt             key                     shell.php
 buildings.png              dds1-alpine.flag.img.gz   flag.txt.enc         key_file                ukn_reality.jpg
 capture.pcap               disk.flag.img             flag2.txt.enc        myNetworkTraffic.pcap   unknown.zip
 capture.pcap.1             disk.flag.img.gz.1        fundamentosciber     picopico.key
marcorojas@MarcoRojas:~$ ls challenge.zip
challenge.zip
marcorojas@MarcoRojas:~$ unzip challenge.zip
Archive:  challenge.zip
   creating: home/ctf-player/drop-in/
 extracting: home/ctf-player/drop-in/flag.png
marcorojas@MarcoRojas:~$ ls
'Forensics is fun.pptm'     challenge.zip             disk.flag.img.gz.2   hash                    picopico.key
'Forensics is fun.pptm.1'   cookies                   disk.img             heapdump                retos
'Forensics is fun.pptm.2'   dds1-alpine.flag.img      flag.txt             home                    server.py
 buildings.png              dds1-alpine.flag.img.gz   flag.txt.enc         key                     shell.php
 capture.pcap               disk.flag.img             flag2.txt.enc        key_file                ukn_reality.jpg
 capture.pcap.1             disk.flag.img.gz.1        fundamentosciber     myNetworkTraffic.pcap   unknown.zip
marcorojas@MarcoRojas:~$ cd home
marcorojas@MarcoRojas:~/home$ ls
ctf-player
marcorojas@MarcoRojas:~/home$ cd ctf-player/
marcorojas@MarcoRojas:~/home/ctf-player$ ls
drop-in
marcorojas@MarcoRojas:~/home/ctf-player$ cd drop-in/
marcorojas@MarcoRojas:~/home/ctf-player/drop-in$ ls
flag.png 

al poner el siguiente comando 
marcorojas@MarcoRojas:~/home/ctf-player/drop-in$ eog flag.png

(eog:773): EOG-WARNING **: 13:47:54.642: Couldn't load icon: Icon 'image-loading' not present in theme Adwaita
me arroja un  codigo Qr al escanearlo me da la bandera 


picoCTF{p33k_@_b00_a81f0a35}