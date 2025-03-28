#### Description

There is some interesting information hidden around this site [http://mercury.picoctf.net:39491/](http://mercury.picoctf.net:39491/). Can you find it?

Detalles: ir a la pagina que se muestra en la descripción, ir al codigo fuente y ahi se encontrara la primera parte de la bandera: 

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_f7ce8828}

para encontrar la 3era parte de la bandera agregar 
 <head>
    <title>Scavenger Hunt</title>
    <link href="https://fonts.googleapis.com/css?family=Open+Sans|Roboto" rel="stylesheet">
    <link rel="stylesheet" type="text/css" href="mycss.css">
    <script type="application/javascript" src="myjs.js"></script>
  </head>
 <head>
    <title>Scavenger Hunt</title>
    <link href="https://fonts.googleapis.com/css?family=Open+Sans|Roboto" rel="stylesheet">
    <link rel="stylesheet" type="text/css" href="mycss.css">
    <script type="application/javascript" src="myjs.js"></script>
  </head>
 [http://mercury.picoctf.net:39491/]robots.txt 
 y ahi estara la 3ra parte de la bandera 

para la parte 4 agregar lo siguiente al url de la pagina de la siguiente forma 
http://mercury.picoctf.net:39491/.htaccess

 y para la 5ta y ultima parte de la bandera poner lo siguiente a la url de la siguiente forma
 
  http://mercury.picoctf.net:39491/DS_Store 
  y ahi estara la ultima parte de la bandera 
  
