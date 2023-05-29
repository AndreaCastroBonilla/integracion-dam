# Desarrollo

## DISEÑO

Los bocetos de las actividades fueron realizados a papel. En la elección de la gama cromática, los iconos, fondos y el resto de detalles se emplearon distintas fuentes de licencias gratuitas:
  + **Pantone:** *[PaletteMaker](https://palettemaker.com/app) y [ColorPicker](https://imagecolorpicker.com/)*
  + **Fondos:** *[Freepik](https://www.freepik.es/)*
  + **Iconos:** *[FlatIcon](https://www.flaticon.com/)*
  + **Logo:** *[Canva](https://www.canva.com/es_es/)*
  
En cuanto al diseño funcional de la aplicación, se empleó [StarUML](https://staruml.io/) para la creación de diagramas, además de esquemas orientativos y [DB Browser for SQLite](https://sqlitebrowser.org/) para la base de datos. 

![Peaky Blinders](https://github.com/AndreaCastroBonilla/integracion-dam/assets/96080740/107efdb3-06bf-4897-9802-ac9c00310e8a)
![icono](https://github.com/AndreaCastroBonilla/integracion-dam/assets/96080740/feaff228-ad20-4d7b-b6fa-d33e924cdf45)

### Android Studio
El inicio de la aplicación cargará mediante una SplashScreen; mientras que, la vista principal se compone de un NavigationDrawer con un menú lateral de opciones. Cada una de ellas redirige a su actividad correspondiente, donde el usuario puede realizar una función distinta.
  -	**Closet:** *vista principal donde se puede sacar foto de las prendas.*
  -	**Wish List:** *formulario que se rellenará cada vez que se desee comprar algo.*
  -	**Filter:** *lista con nuestro formulario de deseos. Al pulsar en las opciones, se cargará otra actividad con una lista de tiendas.*
  -	**Map:** *nos llevará al mapa para buscar las tiendas más cercanas.*
  -	**Weather:** *permitirá saber el tiempo en nuestra localización de destino.*

Todas las Activities tienen un layout general donde se encapsulan los distintos elementos, dependiendo de su función. Uno de ellos será el título, idéntico en todas -> color:`#86AABA` | fuente: *cursive*

  -	**Closet:** *FrameLayout [TextView, ImageView, FabButton]*
  -	**Wish List:** *LinearLayout [TextView, EditText, Button]*
  -	**Filter:** *LinearLayout [TextView, RecyclerView]*
  -	**Map:** *ConstraintLayout [WebView]*
  -	**Weather:** *ConstraintLayout [WebView]* 

## IMPLEMENTACIÓN

En la implementación se ha usado exclusivamente Java como lenguaje de programación. En líneas generales, todas las clases cuentan con un método para navegar por las opciones del menú *(onNavigationItemSelected(@NonNull MenuItem item))* y una constante que actúa como ID para asignarles un orden *(private final static int CONT_ACTIVIDAD = 0;)*. Particularidades a destacar:

### Closet
  1. *Permiso para acceder a la cámara en el AndroidManifest.xml.*
  2. *Métodos para abrir la cámara, comprobar los permisos y mostar la foto.*
  
    goToCamera(), onActivityResult(int requestCode, int resultCode, @Nullable Intent data), onRequestPermissionsResult(int requestCode, @NonNull String[] permissions, @NonNull int[] grantResults)

### Wish List
  1. *Método para controlar la validez de los parámetros indoducidos en la lista, no pudiendo ser estos vacíos.*
  
    onClick(View v)
  2. *Método para limpiar los campos una vez los datos introducidos sean correctos.*
  
    clean()
  3. *Clase DBCloset.java encargada de definir la estructura de la base de datos, hija de DBHelper.class, clase donde se implementaron los métodos para crearla y actualizarla.*
    ![estructura](https://github.com/AndreaCastroBonilla/integracion-dam/assets/96080740/3f815090-3d71-4720-b11a-6d752404839f)

### Filter
  1. *Clase Adapter.java que se emplea para definir la manera en la que se mostrarán los datos en el RecyclerView mediante el uso de un ArrayList de Clothes.java, que establece, a su vez, la estructura que tendrá cada prenda almacenada (id, nombre de la tienda, descripción y precio).*

### Map y Weather
  1. *WebView para incrustar la vista del [mapa](https://www.google.com/maps/@28.30421,-16.5235068,10.3z?authuser=1), así como la del [tiempo](https://www.aemet.es/es/eltiempo/prediccion/municipios/tacoronte-id38043).*
