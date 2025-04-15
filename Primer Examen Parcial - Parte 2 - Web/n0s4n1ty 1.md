
Descripción
Un desarrollador ha añadido la función de subir fotos de perfil a un sitio web. Sin embargo, la implementación presenta fallas, lo que representa una oportunidad para ti. Tu misión, si decides aceptarla, es navegar a la página web proporcionada y localizar el área de subida de archivos. Tu objetivo final es encontrar la bandera oculta en el /rootdirectorio.


¡Puedes acceder a la aplicación web aquí !


nos da un link asi que accedemos  y como nos dice, vamos a tener que seguir la ruta que nos asigna al subir la foto, a los archivos

podemos hacer un backdoor para poder entrar en la direccion de las paginas

asi que usamos locate simple-backdoor en una carpeta 
subimos el archivo que hicimos 
y en el link de la ruta vamos a usar el link que nos genero para acceder con los archivos

pero no nos deja modificar archivos, asi que en las pistas nos aparece este interesante ayuda

Siempre que obtenga un shell en una máquina remota, verifiquesudo -l

asi que usamos el sudo -l para ver que usuario tiene permiso para acceder 
asu que completamos con sudo cat/root/flag.txt
para que nos de la bandera

picoCTF{wh47_c4n_u_d0_wPHP_a4ca6ea0}

Bandera

picoCTF{wh47_c4n_u_d0_wPHP_a4ca6ea0}

Referenccias

https://www.youtube.com/watch?v=RawY672j488