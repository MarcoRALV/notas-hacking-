
Description
We found this packet capture and key. Recover the flag.

Detalles: descargamos el reto en nuestra terminal 
wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap
tambien la key 
 wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key
luego vamos con 
tshark -r capture.pcap
openssl rsa -in picopico.key -text
tshark -r capture.pcap  -o "ssl.debug_file:ssldebug.log" -o "ssl.desegment_ssl_records: TRUE" -o "ssl.desegment_ssl_application_data: TRUE" -o "ssl.keys_list:172.31.22.220,443,http,picopico.key" -qz follow,ssl,ascii,0
Running as user "root" and group "root". This could be dangerous.
root@kali:/media/sf_CTFs/pico/WebNet1# mkdir out
root@kali:/media/sf_CTFs/pico/WebNet1# tshark -r capture.pcap  -o "ssl.debug_file:ssldebug.log" -o "ssl.desegment_ssl_records: TRUE" -o "ssl.desegment_ssl_application_data: TRUE" -o "ssl.keys_list:172.31.22.220,443,http,picopico.key" -o "tcp.desegment_tcp_streams: TRUE" -o "tcp.no_subdissector_on_error: FALSE" --export-objects "http,out"

ls out
strings out/vulture.jpg | grep pico



picoCTF{honey.roasted.peanuts}