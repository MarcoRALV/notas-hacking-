#### Description

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag. 


Detalles: Para encontrar esta bandera lo que tenemos que hacer es descargar el archivo que se nos proporciona en el  reto después lo abrimos con wireshark (es un analizador de protocolos de red de código abierto que permite capturar y analizar el tráfico de red) una ves echo esto, en nuestra terminal de linux ponemos lo siguiente 
 wireshark capture.pcap &  una ves realizado esto seguimos el trafico y encontramos la bandera en el stream numero 6
 
picoCTF{StaT31355_636f6e6e}
