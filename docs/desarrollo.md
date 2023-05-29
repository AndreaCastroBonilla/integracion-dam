# Desarrollo

## DISEÑO

Los bocetos de las actividades fueron realizados a papel. En la elección de la gama cromática, los iconos, fondos y el resto de detalles se emplearon distintas fuentes de licencias gratuitas:
  + Pantone: [PaletteMaker](https://palettemaker.com/app) y [ColorPicker](https://imagecolorpicker.com/)
  + Fondos: [Freepik](https://www.freepik.es/)
  + Iconos: [FlatIcon](https://www.flaticon.com/)
  + Logo: [Canva](https://www.canva.com/es_es/)
En cuanto al diseño funcional de la aplicación, se empleó StarUML para la creación de diagramas, además de esquemas orientativos.
![Peaky Blinders](https://github.com/AndreaCastroBonilla/integracion-dam/assets/96080740/107efdb3-06bf-4897-9802-ac9c00310e8a)
![icono](https://github.com/AndreaCastroBonilla/integracion-dam/assets/96080740/feaff228-ad20-4d7b-b6fa-d33e924cdf45)

### Android Studio
El inicio de la aplicación cargará mediante una SplashScreen; mientras que, la vista principal se compone de un NavigationDrawer con un menú lateral de opciones. Cada una de ellas redirige a su actividad correspondiente, donde el usuario puede realizar una función distinta.
  -	Closet: vista principal donde se puede sacar foto de las prendas.
  -	Wish List: formulario que se rellenará cada vez que se desee comprar algo.
  -	Filter: lista con nuestro formulario de deseos. Al pulsar en las opciones, se cargará otra actividad con una lista de tiendas.
  -	Map: nos llevará al mapa para buscar las tiendas más cercanas.
  -	Weather: permitirá saber el tiempo en nuestra localización de destino.

Todas las Activities tienen un layout general donde se encapsulan los distintos elementos, dependiendo de su función. Uno de ellos será el título, idéntico en todas.
> color:`#86AABA` | fuente: *cursive*
