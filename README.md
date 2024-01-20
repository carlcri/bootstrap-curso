# bootstrap-curso
Curso de Bootstrap *free code camp*:

**Version 5.2 de Bootstrap**

https://www.youtube.com/watch?v=QCw0L6FupQ0&t=354s 

Instructora:  Estefania Cassingena Navone

# Introduccion 
time (36:28)

Bootstrap es un framework CSS para desarrollar sitios WEB adaptables(responsivos).

Un framework es una estructura(base) que puedes usar para desarrollar tu aplicacion o sitio WEB de manera mas rapida y eficiente.

## Framework CSS

*Clases* que nos permiten personalizar el estilo de los elementos HTML del sitio WEB.

## Responsive

En español adaptable o responsivo, que se adapta a distintos dispositivos  en base a su tamaño  y orientacion(en desarrollo web).

![](https://i.imgur.com/ECTQ2h1.png)

Si queremos ver el diseño responsivo, vamos por ejemplo a *https://www.freecodecamp.org/* en *Chrome*, inspeccionar y:

![](https://i.imgur.com/vIA3R9y.png) 

e inmediatamente cambia la distribucion de los elementos. Igualmente si el dispositivo se rota, la pagina debe verse bien.

![](https://i.imgur.com/eNNG71B.png)

Y sobre esa misma barra se puede visualizar para un dispositivo en especifico, Samsung, Iphone, desplegando ese menu:

![](https://i.imgur.com/57yfG0f.png)

# Tres Pilares de Bootstrap

![](https://i.imgur.com/jrw8md3.png)

- Componentes: elementos html reutilizables
- Iconos de Bootstrap Iconos

# La GRID de Bootstrap

En español *cuadricula*, que permitira definir como es que se quieren se presenten los elementos de la pagina Web.

GRID: Conjunto de contenedores, filas y columnas que definen como se va presentar y alinear el contenido. Veamos algunos ejemplos:

![](https://i.imgur.com/rPU0dRx.png)
Tres Columnas con tres filas

![](https://i.imgur.com/KBVprXs.png)
Donde algunos elementos ocupan mas espacios que otros

![](https://i.imgur.com/nmoS6ra.png)
Tambien solo tres columnas

Un concepto muy importante de *Bootstrap* es entender que cada fila esta dividida en 12 columnas, que nos permitira crear todas esas combinaciones vistas anteriormente.

![](https://i.imgur.com/XF59d4h.png)

## Clases especificas para la GRID

Filas:

- row

Columnas:

- col-
- col-sm-
- col-md-
- col-lg-
- col-xl-

### row

Cuando agregamos la clase *row* ese elemento html, se va convertir en una fila para *Bootstrap*. Por ejemplo

```html
<div class="row">

</div>
```
Luego tenemos que especificar las columnas

    xs: extra small
    sm: small
    md: medium
    lg: large
    xl: extra large

![](https://i.imgur.com/6UEAkdP.png)
donde px son pixeles.

¿A que se refiere Bootstrap con todas estas abrevicaciones?

Hace referencia de la ventana desde donde se esta visualizando la pagina Web. En ingles es *VIEWPORT*

- xs: la dimension xs aplica cuando el dispositivo es menor que 576px. Y asi sucesivamente para las otras dimensiones.

# Breakpoints en Boostrap

Cada una de esas dimensiones representa un *breakpoint*, o un punto de quiebre, o una dimension(ancho) a partir de la cual podemos cambiar el estilo o la estructura de la pagina Web.

Para el caso de Boostrap, tenemos seis breakpoints prederminados que fueron los vistos anteriormente, pero tambien tenemos *breakpoints personalizados*:

Por ejemplo cuando pasamos de 500 a 501 es evidente el cambio de estilo:

![](https://i.imgur.com/RHMR79N.png)
Con 500.

![](https://i.imgur.com/1TqsLDl.png)
Con 501

Y cuando pasa de 600 a 601, es evidente el cambio en la barran de navegacion, donde en lugar de icono, aparece *Menu*

![](https://i.imgur.com/fiW0bbK.png)

## ¿A que clases corresponde cada uno de estos Breakpoints?

Importante el punto, para no confundirlos con otra cosa, un id por ejemplo. 

![](https://i.imgur.com/aAp5WUn.png)

1. Para xs, simplemente colocamos *.col-*
2. Para todas las demas *.com-sm-*, *.col-md-* y asi sucesivamente

Por ejemplo, *.col-sm-4* especificara el breakpoint *sm* y que ocupe 4 de las 12 columnas de la grid

# Estructura de la GRID de Bootstrap

Un contenedor puede contener filas y cada columna contiene 12 columnas. Ese contenedor nos va permitir contener esa estructura de filas y columnas. 

En Bootstrap tenemos clases prederminadas como *container*, *row* y *col*:

```html
<div class="container">
    <div class="row">
        <div class="col"></div>
        <div class="col"></div>
    </div>

    <div class="row">
        <div class="col"></div>
        <div class="col"></div>
        <div class="col"></div>
    </div>
</div>
```
Por ejemplo aqui tenemos un contenedor principal, y dos filas, donde la primera tiene dos columnas, y la segunda tres columnas.

![](https://i.imgur.com/Jf5RSqS.png)

# Contenedores en Bootstrap

Un contenedor en Bootstrap es un elemento html que va contener toda la estructura, en Bootstrap exiten dos:

- .container: crea un contenedor responsivo con un **ancho maximo fijo** que depende del tamaño del dispositivo

- .container-fluid: es un contenedor responsivo que cubre el 100% el ancho de la ventana. 

## Ejemplo

FOLDER *1_ejemplo*

Creamos un *index.html*, donde necesitamos incluir *Bootstrap*. Veamos que dice la documentacion, usaremos la version del instructor 5.2

https://getbootstrap.com/ 

https://getbootstrap.com/docs/5.2/getting-started/introduction/ 

Ir a download y CDN via jsDelivr, CDN significa Content Delivery Network, permite tener dichos archivos en la pagina sin que sean archivos locales. Es decir, se van a descargar al momento que la persona acceda a la pagina Web que estamos creando. 

![](https://i.imgur.com/OsKDjZS.png)

Copialos en el *head*.

Asignamos un estilo basico del *div* con un color de fondo morado, y letras blancas. A medida que se van probando dispositivos mas pequeños, el contenedor se va reajustando, porque tiene un ancho maximo para cada tipo de dispositivo, pero sin llenar el 100% de la ventana. 

![](https://i.imgur.com/SzbW2CF.png)

Mientras que *container-fluid* siempre ocupara el 100% de la pantalla

![](https://i.imgur.com/lVEntey.png)

## Containers responsivos

Tambien tenemos contenedores responsivos, que van a cubrir el 100% de la ventana hasta que llegan al denominado *breakpoint*:

- container-sm
- container-md(no funciono)
- container-lg(funciono)

Por ejemplo si tenemos container-lg, va cubrir el 100% de la ventana hasta que llegue al breakpoint, va a convertirse en un contenedor con un ancho maximo. 

# Estructura de la Grid Filas y Columnas

FOLDER: *2_ejemplo*

Los elementos de las filas pueden ocupar varias columnas. Por ejemplo, tenemos dos elementos html uno al lado de otro, cuando llegue al breakpoing *sm*, el primer elemento ocupara 5 columnas, y el segundo 7. 

![](https://i.imgur.com/7o7UPk5.png)

Las columnas de los elementos de una fila deben sumar 12. Aqui tendremos una fila con 2 columnas y otra con 3. Sin colocarle estilos se veria asi:

![](https://i.imgur.com/HWy0ea4.png)

Con estilos:

![](https://i.imgur.com/NtbWPbk.png)

Como solo especificamos *col*, todas las columnas trataran de tomar una distribucion uniforme. 

Bootstrap tambien nos permite centrar el texto, sin usar css, simplemente añadiendo la clase *text-center*

![](https://i.imgur.com/ZGX3Ukw.png)

Fijate que para un viewport menor o igual a 991, habra un cambio:

![](https://i.imgur.com/4D1Q9dL.png)

1:30:29












