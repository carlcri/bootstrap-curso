# Flexbox

ver: *6_flexbox*.

CSS Flexible Box Layout. Permite que los elementos responsivos ubicados dentro de un contenedor se distribuyan automaticamente en base al tamaño del dispositivo.

No van estar los elementos estaticos y con un ancho especifico, con una una distribucion especifica. Bootstrap incluye clases que podemos usar  para trabajar con Flexbox mas facilmente. 

## ¿Cual es el proposito de Flexbox?

Tenemos tres elementos html como divs, imagenes, esos elementos van a estar contenidos en un contenedor, y ese contenedor lo llamaremos de ahora en adelante *Flex*:

![](https://i.imgur.com/ZkcNEtR.png)

Si trabajamos con un contenedor Flexbox usando html y css lo hariamos de la siguiente forma:

Creando nuestra propia clase *contenedor*, y a ese contenedor tocaria asignarle la propiedad *css* *display* con el valor *flex*:

![](https://i.imgur.com/DZdsU0L.png)

Pero con Bootstrap es mucho mas sencillo, con solo asignar la clase *.d-flex*, se crearia un contenedor flexible:

![](https://i.imgur.com/jephLZ8.png)

No veremos todos los aspectos de *Flexbox*, algunos para que los puedas usar en este proyecto.

### flex-direction

Esta propiedad extablece el eje principal del contenedor, la *direccion* en la cual se van a colocar los elementos dentro del contenedor.

Es decir se van a poder alinear los elementos de manera horizontal o vertical:

- row: el eje principal seria horizontal

![](https://i.imgur.com/6ZtkAco.png)

- row reverse: a diferencia del anterior, el eje principal seria vertical

![](https://i.imgur.com/nPvdFm0.png)

- column
- column 
- column-reverse

A partir de como se defines los ejes principales, la propiedad *justify-content* define como se distribuyen los elementos de acuerdo al eje principal. 

![](https://i.imgur.com/CKLGmSz.png)

Estas propiedades CSS, tienen su equivalente en *Bootstrap*, donde las podremos implementar mas rapidamente, con estas clases que ya vienes predeterminadas:

![](https://i.imgur.com/Q2HBXSh.png)

Otra propiedad seria *align-items*, que define como se distribuye los elementos en el eje perpendicular  al eje principal. *align-items* tambien tiene su equivalente en *Bootstrap*.

![](https://i.imgur.com/dZhx50z.png)

Y su equivalente en Bootstrap:

Normalmente el que se usa es *center*.

![](https://i.imgur.com/Ah3ST0B.png)

Con la propiedad css *flex-wrap* se determina si los elementos deben ser ajustados para que siempre esten en una misma linea o si se les permite distribuirse en varias lineas si es necesario.

Si por ejemplo, *flex-wrap* tiene el valor por defecto *nowrap*, es decir que no deberian distribuirse, y el dispositivo es mas pequeño, los elementos se van a comprimir. 

![](https://i.imgur.com/gpgp0t7.png)

Pero si se le asigna ahora wrap a flex-wrap, estos elementos se van a reajustar, como por ejemplo estaran dentro del mismo contenedor pero ocupando varias lineas. 

![](https://i.imgur.com/KpnmrW0.png)

En Bootstrap tendrian su equivalente:

![](https://i.imgur.com/nPf5FFq.png)

# Añadir Bootstra al Proyecto

Ya completamos la parte teorica, y trabajaremos en nuestro sitio Web de portafolio. Incluimos dos elementos como lo hemos venido haciendo donde uno corresponde a css, y el otro a Js. 

![](https://i.imgur.com/PPM5BPH.png)

Sin embargo la documentacion de Bootstrap nos recomiendo incluir la parte que corresponde a *Js* al final de la etiqueta *body*:

![](https://i.imgur.com/3piZog9.png)

Y crearemos una hoja de estilos, y la vinculamos al html mediante otro tag de *link*:

```html
<link rel="stylesheet" href="./estilos.css">
```

Donde *href* indica donde esta el archivo, y *rel* indica la relacion entre el archivo html y css, en este caso, es de estilos. 

# Favicon y Metadatos

Ver *7_proyecto*

Hay una etiqueta llamada *meta* como por ejemplo la codificacion de los caracteres, que se indica con el atributo *charset*, para nuestro caso *utf-8*.

- se añade metadato de author y descripcion.
- se añade el de palabras clave: *keywords*: secuencia de palabras clave separadas por una coma.
- muy importante: **viewport**, que en español seria algo asi como la ventana del navegador. Para que se ajuste al tamaño del dispositivo. 

```html
    <meta charset="utf-8">
    <meta name="author" content="Gustavin Pinguin">
    <meta name="description" content="Portafolio de Desarrollo Web de Gustavin Pinguin">
    <meta name="keywords" content="HTML, CSS, JavaScript, React">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
```

## Personalizando el icono y el titulo.

- tag *title*
- tag *favicon*

Probe descargando un icono de los de Bootstrap y funciono, pero usare el de la instructora:

```html
<link rel="icon" type="image/x-icon" href="./static/images/icono.png">
```

# Barras de navegacion

Ver *7_proyecto*