# 📲 Anteproyecto

## OBJETIVOS

El objetivo de este proyecto será poder registrar nuestro armario de forma virtual, almacenando nuestras prendas, complementos y zapatos de manera que podamos crear combinaciones sin necesidad de verlas en persona. Adicionalmente, también se podrán usar aquellas que estén disponibles en tienda y deseemos comprarlas, pues se dispondrá de una lista de deseos.

## ANÁLISIS DEL SOFTWARE

Requisitos:

1. *Almacenar prendas mediante fotos hechas con el dispositivo o a través de las tiendas online.*

2. *Tener acceso a las webs de las tiendas desde la propia aplicación.*

3. *Crear una lista de deseos con los productos de la búsqueda online (punto anterior) mediante la cumplimentación de un formulario.*

4. *Clasificar los conjuntos creados, con prendas propias o de la lista de deseos, según las necesidades del usuario: tiempo, estilo, ocasión...*

5. *Tener acceso a la ubicación del dispositivo para ver qué tiendas son las más cercanas a nuestra posición actual.*

6. *Acceder al tiempo de la localización deseada.*

![Use Cases](https://user-images.githubusercontent.com/96080740/226205366-f6c6a685-58ba-40b2-a048-7dfc706a27d9.jpg)

## DISEÑO DEL SOFTWARE

La implementación se llevará a cabo desde Android Studio, empleando Java y JavaScript como lenguajes de desarrollo. Constará, en un inicio, de tres paquetes:

1. **Main Package:** *contendrá la vista principal, desde donde se podrá acceder al resto de funcionalidades, notas del desarrollador y posibles opciones extras.*

2.	**DB Package:** *almacenará todas las clases relacionadas con la base de datos.*

    *a.	Helper – creación y estructura.*
    
    *b.	DataBase – métodos de modificación, inserción, eliminación…*
    
    *c.	Adapter – adaptador para el mostrado de la información.*
    
3. **Fragments Package:** *el resto de las clases se encontrarán en este paquete, ya que no necesitarán, a priori, de otras auxiliares para su correcto funcionamiento.*

![Add a little bit of body text](https://user-images.githubusercontent.com/96080740/226205046-b981f1f6-4f58-4f56-b6bd-f6c3e0e01e81.jpg)

## ESTIMACIÓN DE COSTES

La creación de este proyecto solo contará con un coste temporal de dos meses aproximadamente, pues no será necesario la contratación de ningún servicio.
