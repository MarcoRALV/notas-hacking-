#### Description

Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:53554/](http://mercury.picoctf.net:53554/)

Detalles: copear el url de la pagina, pegarlo en nuestro entorno de desarrollo y agregarle el curl -I 



marcorojas@MarcoRojas:~$ curl -I Post http://mercury.picoctf.net:53554/index.php
curl: (6) Could not resolve host: Post
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_2e5ba39f}
Content-type: text/html; charset=UTF-8

marcorojas@MarcoRojas:~$
