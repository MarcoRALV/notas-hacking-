#### Description

The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/98/flag2of2-final.pdf).

detaalles : 
descargamos el reto marcorojas@MarcoRojas:~$ wget https://artifacts.picoctf.net/c_titan/98/flag2of2-final.pdf
--2025-05-11 13:56:49--  https://artifacts.picoctf.net/c_titan/98/flag2of2-final.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.26, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3362 (3.3K) [application/octet-stream]
Saving to: ‘flag2of2-final.pdf’

flag2of2-final.pdf            100%[=================================================>]   3.28K  --.-KB/s    in 0s

2025-05-11 13:56:49 (373 MB/s) - ‘flag2of2-final.pdf’ saved [3362/3362]


y vamos a 


marcorojas@MarcoRojas:~$ ls
'Forensics is fun.pptm'     cookies                   flag.txt             home                    shell.php
'Forensics is fun.pptm.1'   dds1-alpine.flag.img      flag.txt.enc         key                     ukn_reality.jpg
'Forensics is fun.pptm.2'   dds1-alpine.flag.img.gz   flag2.txt.enc        key_file                unknown.zip
 buildings.png              disk.flag.img             flag2of2-final.pdf   myNetworkTraffic.pcap
 capture.pcap               disk.flag.img.gz.1        fundamentosciber     picopico.key
 capture.pcap.1             disk.flag.img.gz.2        hash                 retos
 challenge.zip              disk.img                  heapdump             server.py
marcorojas@MarcoRojas:~$ ls flag2
ls: cannot access 'flag2': No such file or directory
marcorojas@MarcoRojas:~$ ls flag2of2-final.pdf
flag2of2-final.pdf 
marcorojas@MarcoRojas:~$ convert flag2of2-final.pdf flag2of2-final.png
marcorojas@MarcoRojas:~$ ls
'Forensics is fun.pptm'     cookies                   flag.txt             heapdump                server.py
'Forensics is fun.pptm.1'   dds1-alpine.flag.img      flag.txt.enc         home                    shell.php
'Forensics is fun.pptm.2'   dds1-alpine.flag.img.gz   flag2.txt.enc        key                     ukn_reality.jpg
 buildings.png              disk.flag.img             flag2of2-final.pdf   key_file                unknown.zip
 capture.pcap               disk.flag.img.gz.1        flag2of2-final.png   myNetworkTraffic.pcap
 capture.pcap.1             disk.flag.img.gz.2        fundamentosciber     picopico.key
 challenge.zip              disk.img                  hash                 retos
marcorojas@MarcoRojas:~$ eog flag2of2-final.png 



picoCTF{f1u3n7_1n_pn9_&_pdf_1f991f77}