
#### Description

Additional details will be available after launching your challenge instance. 


Detalles: Tenemos que iniciar el programa de Burp Suite y activa el Foxy Proxy luego tenemos que accede al sitio web del desafío http://titan.picoctf.net:57033/  a continuación interceptar la solicitud cuando la página intente cargar, Burp interceptará la solicitud HTTP y envía la solicitud al Repeater luego tenemos que  cambiar el método HTTP de GET a POST
envía la solicitud modificada la respuesta debería contener la flag en el cuerpo o en los headers 
picoCTF{#0TP_Bypvss_SuCc3$S_b3fa4fla}