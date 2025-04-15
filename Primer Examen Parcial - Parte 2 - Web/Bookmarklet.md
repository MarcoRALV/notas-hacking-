
Description
Why search for the flag when I can make a bookmarklet to print it for me?
Browse here, and find the flag!


nos da un link para acceder asi que lo abrimos

algunas pistas que nos da son 
-A bookmarklet is a bookmark that runs JavaScript instead of loading a webpage.
-Web browsers have other ways to run JavaScript too.


al acceder vemos que tiene un codigo 
  javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓË¨ËÓ§Èí";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();

asi que inspeccionamos la pagina
y en la parte de consola ponemos ese codigo y lo ejecutamos 
y nos da la bandera
picoCTF{p@g3_turn3r_e8b2d43b}


BANDERA

picoCTF{p@g3_turn3r_e8b2d43b}



Referencias
https://www.youtube.com/watch?v=XkVmpUW5-IA&ab_channel=get__pismed

