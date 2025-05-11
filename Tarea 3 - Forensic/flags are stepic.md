#### Description

A group of underground hackers might be using this legit site to communicate. Use your forensic techniques to uncover their message

Additional details will be available after launching your challenge instance.
Finalmente, me di cuenta de que el título del desafío tenía la pista todo el tiempo: "Las banderas son **espáticas".**

[Stepic](https://pypi.org/project/stepic/) es un módulo de Python utilizado para esteganografía y probablemente se usó para ocultar la bandera dentro de esta imagen.

Escribí un pequeño script en Python, gracias a esta publicación [de StackOverflow](https://stackoverflow.com/questions/16838341/steganography-in-python-stepic) , para decodificar el mensaje:

desde PIL importar Imagen   
importar stepic   
  
im1 = Imagen. open ( 'upz.png' )   
s = stepic.decode(im1)   
imprimir (s)

Y encontré la bandera
picoCTF{fl4g_h45_fl4g9a81822b}