
Description
We found this packet capture and key. Recover the flag.

Detalles: descargamos el reto en nuestra terminal 
wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap
tambien la key 
 wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key

y vamos con el comando 
tshark -r capture.pcap 
y luego usamos 
openssl rsa -in picopico.key -text 
tshark -r capture.pcap  -T fields -e tcp.stream | sort -u 
tshark -r capture.pcap  -qz follow,tcp,ascii,0 
tshark -r capture.pcap  -qz follow,ssl,ascii,0
tshark -r capture.pcap  -o 
La bandera se envía como uno de los encabezados HTTP:


Pico-Flag: picoCTF{nongshim.shrimp.crackers}



