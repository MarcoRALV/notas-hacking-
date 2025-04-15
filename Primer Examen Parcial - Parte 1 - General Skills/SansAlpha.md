Description
The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.
ssh -p 50684 ctf-player@mimas.picoctf.net
Use password: 83dcefb7


Vamos a iniciar sesion con el link y la contraseña que nos proporcionaron
ssh -p 50684 ctf-player@mimas.picoctf.net
Use password: 83dcefb7

Intentamos con 
SansAlpha$ /*
bash: /bin: Is a directory

asi que intentamos con
y nos sale 
SansAlpha$ /*/??????
/bin/base32: extra operand ‘/bin/base64’
Try '/bin/base32 --help' for more information.

A lo cual agregaremos 
SansAlpha$ /*/????64 */*
/bin/base64: extra operand ‘/bin/x86_64’
Try '/bin/base64 --help' for more information.
y poniendo este comando nos da un codigo que suponemo que sera nuestra bandera  
SansAlpha$ /*/???[!_]64 */????.*
cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV8zNmE2NzRjMH0=

SansAlpha$     
asi que vamos a cyberchef a ver que nos arroja 
y nos da la bandera

return 0 picoCTF{7h15_mu171v3r53_15_m4dn355_36a674c0}


Bandera

picoCTF{7h15_mu171v3r53_15_m4dn355_36a674c0}





Notas adicionales 
Wildcards



Referencias
https://www.youtube.com/watch?v=ITTdaIh5mjA

