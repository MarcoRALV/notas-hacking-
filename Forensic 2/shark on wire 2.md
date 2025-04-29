

#### Description

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

Detalles:Vemos que, en la información de cada paquete, hay un número de 4 dígitos que empieza por el 5. Si tomamos los últimos 3 dígitos de cada número, según el orden de llegada de los paquetes, y los convertimos a ASCII, obtenemos nuestra bandera.


picoCTF{p1LLf3r3d_data_v1a_st3g0}

Apoyo : https://github.com/kevinjycui/picoCTF-2019-writeup/blob/master/Forensics/shark%20on%20wire%202/README.md