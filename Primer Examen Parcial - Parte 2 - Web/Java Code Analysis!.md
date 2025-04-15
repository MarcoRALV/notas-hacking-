

#### Description

BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!

Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/478/bookshelf-pico.zip).Website can be accessed [here!](http://saturn.picoctf.net:51047/).



Detalles: vamos a la web proporcionada y vamos a inspeccionar la pagina, vamos al apartado de apliacation y cliqueamos en local storage, copeamos el token y vamos a jwt.io lo pegamos y modificamos la Signature con : 1234 
en el payload modificamos Free por Admin, el user id lo cambiamos de 1 a 2 y en email cambiamos user por admin, copeamos de vuelta el token y lo pegamos en value y modificamos el payload y listo refrescamos la pagina 

picoCTF{w34k_jwt_n0t_g00d_602ce414} 


fuente:https://www.youtube.com/watch?v=tsTkxWxLTqk&ab_channel=MartinCarlisle

Equipo: Marco Rojas, Brandon Omar, Luis Jesús 