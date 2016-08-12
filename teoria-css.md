# CSS Cascading Style Sheet
**(Hojas de Estilo en Cascada)**

![CSS](http://bextlan.com/img/para-cursos/css-logo.jpg)

## Índice
1. [Sintaxis](#sintaxis)
1. [Selectores](#selectores)
1. [Unidades de Medida](#unidades-de-medida)
1. [Colores](#colores)
1. [Tipografías](#tipografías)
1. [Características CSS3](#características-css3)
1. [Prefijos Navegadores](#prefijos-navegadores)
1. [Modelo de Caja](#modelo-de-caja)
1. [Posicionamiento](#posicionamiento)
1. [Visualización](#visualización)
1. [Técnicas de Maquetación](#técnicas-de-maquetación)
1. [Guías de Estilo](#guías-de-estilos)
1. [Componentes Modulares](#componentes-modulares)
1. [Sistemas de Nomenclaturas](#sistemas-de-nomenclaturas)
1. [Patrones de Diseño](#patrones-de-diseño)
1. [Frameworks](#frameworks)

## Sintaxis
Lenguaje de Presentación basado en reglas con una sintaxis de atributo valor

Provee presentación (diseño) al contenido HTML

Su principal objetivo es separar el contenido (HTML) de su presentación (CSS)

~~~~~~~~~~~~~~
selector {
    atributo-1: valor-1;
    atributo-2: valor-2;
    ...
    atributo-n: valor-n;
}
~~~~~~~~~~~~~~

**[⬆ regresar al índice](#Índice)**


## Selectores
Elemento(s) al que se le aplican reglas CSS

### Selectores Básicos:
* **De Etiquetas** `p { ... }`
* **Identificadores** `#menu { ... }`
* **Clases** `.item { ... }`
* [Más info](http://librosweb.es/libro/css/capitulo_2.html)

### Selectores Avanzados
* **Universal** `* { ... }`
* **Descendiente (espacio en blanco)** `.menu a { ... }`
* **de Hijos** `.menu > li { ... }`
* **de Hermanos** `section ~ article { ... }`
* **Adyacentes** `h1 + h2 { ... }`
* **de Atributos** `input[type="text"] { ... }`
* [Más Info](http://librosweb.es/libro/css_avanzado/capitulo_3.html)
    
### Pseudo-selectores
Nos ayudan a aplicar estilos especiales a nuestros elementos HTML, dependiendo de su contexto, posición o estado

Existen 2 tipos:
* Pseudo-clases
* Pseudo-elementos

#### Pseudo-clases
* **Estatus de Enlaces** `:link :visited`
* **Interacciones del Usuario** `:active :hover :focus`    
* **Elementos de Formularios** `:checked :disabled :in-range :invalid :out-of-range :required :target :valid`
* **Posición del Elemento** `:first-child :first-of-type :last-child :last-of-type :nth-child() :nth-last-child() :nth-of-type() :only-child :only-of-type :default`
* **CSS3** `:dir() :empty :first :fullscreen :indeterminate :lang() :left :not() :optional :read-only :read-write :right :root :scope`
* [Más info](https://css-tricks.com/examples/nth-child-tester/)

#### Pseudo-elementos
* **`::after { content:" " }`**
* **`::before { content:" " }`**
* **`::first-letter`**
* **`::first-line`**
* **`::selection`**

### Especificidad
Es lo que determina que estilo será el que acabará aplicandose a un elemento determinado

Cuando a un elemento se le aplica más de un selector con reglas que actúan sobre la misma propiedad, es la especificidad la encargada de resolver este conflicto

A grandes rasgos podemos ordenar los diferentes tipos de selectores de menor a mayor peso específico de la siguiente manera:

1. Selectores de elemento
1. Selectores contextuales
1. Clases
1. IDs

**[⬆ regresar al índice](#Índice)**


## Unidades de Medida
* **Absolutas** `px, pt, pc, cm, mm, in`
* **Relativas**
    * **al Contenedor** 
        * `% (Porcentajes)`
    * **a la Tipografía**
        * `em` basada en la anchura de la letra M del contenedor
        * `ex` basada en la altura de la letra X del contenedor
        * `rem` es el em del elemento raiz (html)
    * **al Viewport**
        * `vw` anchura del viewport
        * `vh` altura del viewport
        * `vmax` entre vw y vh toma el que tenga mayor valor
        * `vmin` entre vw y vh toma el que tenga menor valor

### Equivalencias entre unidades
* **`100% = 1em = 16px = 12pt`**
* [pxtoem](http://pxtoem.com/)

**[⬆ regresar al índice](#Índice)**


## Colores
Sistemas de Colores:
* **CMYK**: Medios Impresos
* **RGB**: Medios Digitales

En HTML el RGB se maneja en código hexadecimal
* Base 16
* Dígitos del 0-9 y de la A-F
* 6 dígitos, una pareja por cada canal de color
* [HTML Color Codes](http://html-color-codes.info/)

![Colores en HTML](http://bextlan.com/img/para-cursos/colores-hexadecimal.png)

**[⬆ regresar al índice](#Índice)**


## Tipografías
* Locales:
    * Con [@font-face](http://caniuse.com/#search=font-face) y [.woff](http://caniuse.com/#search=woff)
    * [Convertidor de Fuentes](http://www.fontsquirrel.com/tools/webfont-generator)

* Externas:
    * [Google Fonts](https://www.google.com/fonts)
    
* Icónicas
    * [Font Awesome](http://fortawesome.github.io/Font-Awesome/)
    * [IcoMoon](https://icomoon.io/)
    * [FlatIcon - Buscador de Íconos](http://flaticon.com/)
    * [Fontello - Generador de Fuentes Icónicas](http://fontello.com/)

**[⬆ regresar al índice](#Índice)**


## Características CSS3
* [Bordes, colores RGBA, fuentes tipográficas, unidades relativas, sombras y gradientes](http://www.youtube.com/watch?v=p-ZjVEhMt2U)
* [Ajuste de texto, texto en columnas, tamaño de caja, fondos múltiples, área, origen y tamaño de fondo](http://www.youtube.com/watch?v=QYOujpsVvXE)
* [Transformaciones 2D y 3D, transiciones y animaciones](http://www.youtube.com/watch?v=yj93AWX0P_k)

![CSS](http://bextlan.com/img/para-cursos/header-css3.jpg)

**[⬆ regresar al índice](#Índice)**


## Prefijos Navegadores
Cuando los navegadores soportan parcialmente un atributo CSS en ocasiones es necesario aplicar los prefijos:

* **`-ms-`** para Internet Explorer y Edge
* **`-moz-`** para Firefox
* **`-webkit-`** para Chrome, Safari, Opera, iOS y Android Browsers

#### Ejemplo
    -ms-border-radius: 20px;
    -moz-border-radius: 20px;
    -webkit-border-radius: 20px;
    border-radius: 20px;

**[⬆ regresar al índice](#Índice)**


## Modelo de Caja
El modelo de caja o "**box model**" es una de las característica más importante de CSS, ya que condiciona el diseño de la web; hace que todos los elementos de un documento HTML se representen mediante cajas rectangulares. 

CSS controla el aspecto de todas las cajas (contenedores), permite definir la altura y anchura de cada caja, el margen existente entre cajas y el espacio de relleno interior que muestra cada una; además controla la forma en la que se visualizan pero la mayoría no muestran ningún color de fondo ni borde, no son visibles a simple vista

### Partes del modelo de caja:
1. **Contenido**: `content`
1. **Relleno**: `padding`
1. **Borde**: `border`
1. **Imagen de fondo**: `background-image`
1. **Color de fondo**: `background-color`
1. **Margen**: `margin`

![Modelo de Caja](http://bextlan.com/img/para-cursos/modelo-caja-css.jpg)

### Propiedades importantes del modelo de caja:
* **Border**: Borde, es la linea que delimita los elementos divide el margin del padding
* **Padding**: Relleno, distancia interna que hay entre los márgenes del elemento(top,right,bottom,left) y su contenido
* **Margin**: Margen, distancia externa que hay entre los elementos y los márgenes del documento u otros elementos (top,right,bottom,left)
* [Más info](http://librosweb.es/libro/css/capitulo_4.html)

#### Ejemplos de `border`:
    border-width: thin | thick | medium | 10px | 1em;
    border-style: solid | dashed | dotted;
    border-color: #F60 | orange;
    border: thin solid #F60; (shorthand)

#### Ejemplos de `margin` y `padding`:
* 4 márgenes / bordes
* top / bottom = verticales
* left / right = horizontales
* 1 valor = Se aplica a los 4 lados
~~~~~~~~~~~~~~~~~~~~~~~~~~~
    margin: 1em;
    padding: 1em;
~~~~~~~~~~~~~~~~~~~~~~~~~~~
* 2 valores:
    * 1° es para top y bottom
    * 2° es para left y right
~~~~~~~~~~~~~~~~~~~~~~~~~~~
    margin: 1em 2em;
    padding: 0 1em;
~~~~~~~~~~~~~~~~~~~~~~~~~~~
* 3 valores:
    * 1° es para top
    * 2° es para left y right
    * 3° es para bottom
~~~~~~~~~~~~~~~~~~~~~~~~~~~
    margin: 1em auto 2em;
    padding: 2em 0 .5em;
~~~~~~~~~~~~~~~~~~~~~~~~~~~
* 4 valores: En sentido de las manecillas del reloj
    * 1° es para top
    * 2° es para right
    * 3° es para bottom
    * 4° es para left
~~~~~~~~~~~~~~~~~~~~~~~~~~~
    margin: 1em 3em 2em 0;
    padding: 2em 1em 0 .5em;
~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Especificando cada lado
~~~~~~~~~~~~~~~~~~~~~~~~~~~
    margin-top | margin-right | margin-bottom | margin-left
    padding-top | padding-right | padding-bottom | padding-left
~~~~~~~~~~~~~~~~~~~~~~~~~~~

> **Nota**: Los atributos del modelo de caja (`border`, `margin` y `padding`) por defecto aumentarán el ancho (`width`) y alto (`height`) de la misma, es decir el [tamaño de caja](https://css-tricks.com/box-sizing/) (`box-sizing`)

**[⬆ regresar al índice](#Índice)**


## Posicionamiento
* **Estático**: Es el que viene por defecto, un elemento detrás del otro
* **Relativo**: Se desplaza respecto de su posición original
* **Absoluto**: Se desplaza respecto de:
    * la posición del body del documento o 
    * del primer elemento padre relativo que tenga
* **Fijo**: Permite mantener fijo un elemento
* **Flotante**: Convierte un elemento en flotante desplazándolo hasta la zona más a la izquierda o más a la derecha de la posición en la que originalmente se encontraba
* **Pegajoso**: Posicionamiento experimental, permite que el elemento sea relativo o fijo dependiendo del area donde se visualiza
* [Más info](http://librosweb.es/libro/css/capitulo_5.html)

**[⬆ regresar al índice](#Índice)**


## Visualización
* **Visibility:** Afecta la visualización del contenido de una caja
* **Display:** Afecta la visualización de la caja
    * **Tipos de Display Básicos**
        * **`block`:** Ocupa todo el ancho disponible
        * **`inline`:** Ocupa sólo el ancho requerido
        * **`none`:** Quita la caja de la visualización del documento

**[⬆ regresar al índice](#Índice)**


## Técnicas de Maquetación
* **`float: left | right;`**
    * [Más Info](http://librosweb.es/libro/css/capitulo_5/posicionamiento_flotante.html)
* **`display: inline-block;`**
    * [Puedo usarlo](http://caniuse.com/#search=inline-block)
    * [Más Info](https://www.w3.org/TR/2011/REC-CSS2-20110607/visudet.html)
* **`display: table;`**
    * [Puedo usarlo](http://caniuse.com/#search=table)
    * [Más Info](https://www.w3.org/TR/CSS21/tables.html)
* **`display: flex;`**
    * [Puedo usarlo](http://caniuse.com/#search=flex)
    * [Guía Completa de CSS-Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
    * [Más Info Propiedad Flex en CSS-Tricks](https://css-tricks.com/almanac/properties/f/flex/)
    * [Más Info W3C](https://www.w3.org/TR/css-flexbox/)
    * [Más Info MDN](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Flexible_Box_Layout/Usando_las_cajas_flexibles_CSS)
* **`display: grid;`**
    * [Puedo usarlo](http://caniuse.com/#search=grid)
    * [Guía Completa de CSS-Tricks](https://css-tricks.com/snippets/css/complete-guide-grid/)
    * [Grid by Example](http://gridbyexample.com/presentations/)
    * [Más Info W3C](https://www.w3.org/TR/css-grid-1/)

**[⬆ regresar al índice](#Índice)**


## Guías de Estilos
* Genera un código más legible y fácil de mantener
* Disminuye la cantidad de errores
* Refuerza las buenas prácticas
* Permite trabajar en un mismo proyecto a varios desarrolladores
* [Code Guide](http://codeguide.co/)
* [CSS Guidelines](http://cssguidelin.es/)
* [Airbnb CSS / Sass Styleguide](https://github.com/airbnb/css)

### Buenas Prácticas
* Separar nombre de selectores con el guión medio (-) y escribir en minúsculas
* Preferir **`<link>`** sobre **`@import`** para invocar hojas de estilo
* Definir siempre un **`font-size`** al elemento root (**`html`**) y hacerlo en **`px`**
* Ser cuidadoso con la definición de reglas a selectores de etiquetas
* Evitar definición de selectores de identificadores
* Usar en su mayoria selectores de clases
* Aprovechar los pseudo-selectores y unidades de medida disponibles
* Tener precaución con los shorthand de CSS
    * **`padding, margin, font, background, border, border-radius`**
    * preferible **`background-color: #FFF`** que **`background: #FFF`**
* Estandarizar los estilos iniciales de nuestras etiquetas HTML en todos los navegadores
    * [Reset.css](http://meyerweb.com/eric/tools/css/reset/)
    * [Normalize.css](https://necolas.github.io/normalize.css/)
    * Definir uno propio que se adapte a nuestra técnica de maquetación y no te olvides del [box-sizing](http://www.paulirish.com/2012/box-sizing-border-box-ftw/)
* Maquetar bajo un enfoque **Mobile First**

### Ordenamiento Código CSS
#### Selectores
* Ir de lo General a lo Particular (Aprovechar la Cascada CSS)
* Estilos Generales
    * Código CSS para Estandarizar
    * Selectores de Etiqueta
    * Selectores de ID (si hubiera)
    * Selectores de Clases
* Mediaqueries
    * Preferir Mobile First a Desktop First

#### Atributos
Utilizar la fórmula de la **PC-TV**:
* Posicionamiento **`position, top, left, right, bottom, clear, z-index`**
* Modelo de Caja **`display, float, margin, padding, width, height`**
* Tipografía **`font-family, font-size, line-height, color, text-align`**
* Visual **`background-color, border, border-radius, outline, opacity`**

**[⬆ regresar al índice](#Índice)**


## Componentes Modulares
> “It's a repeating visual pattern, that can be abstracted into an independent snippet of HTML, CSS and possibly JavaScript.”
> > [Nicole Sullivan](https://vimeo.com/72759139)

* Son un fragmento de la interfaz que cumple una única función
* Son independientes, tanto de su contexto como del resto de componentes
* Son reutilizables
* Son autocontenidos, no filtran estilos a otros componentes

![Componentes Modulares](http://bextlan.com/img/para-cursos/componentes-css.png)

### Atomic Design
* Metodología basada en: Átomos, Moléculas, Organismos, Plantillas y Páginas
* [Tabla periódica de las etiquetas HTML](http://zqsmm.qiniucdn.com/data/20110511083224/index.html)
* [Artículo](http://bradfrost.com/blog/post/atomic-web-design/)
* [Slides](http://es.slideshare.net/bradfrostweb/atomic-design)
* [Libro](https://github.com/bradfrost/atomic-design)
* [Laboratorio de Patrónes](http://patternlab.io/)
* [Ejemplos](http://demo.patternlab.io/)
![Atomic Design](http://bextlan.com/img/para-cursos/atomic-design.png)

**[⬆ regresar al índice](#Índice)**


## Sistemas de Nomenclaturas

* [OOCSS - CSS Orientado a Objetos](http://oocss.org/)
* [CCSS - Componentes CSS](http://sathify.github.io/CCSS/)
* [SUIT CSS - Utilidades y Componentes CSS](https://github.com/suitcss/suit/blob/master/doc/naming-conventions.md)
* [BEM - Bloque Elemento Modificador](https://en.bem.info/methodology/)

![BEM](http://bextlan.com/img/para-cursos/bem.jpg)

##### Estructura
    .bloque { ... }
    .bloque__elemento { ... }
    .bloque--modificador { ... }

##### Ejemplo
    .menu { ... }
    .menu__item { ... }
    .menu__item--hover{ ... }

**[⬆ regresar al índice](#Índice)**


## Patrones de Diseño
Los patrones de diseño son la base para la búsqueda de soluciones a problemas comunes en el desarrollo de software y otros ámbitos referentes al diseño de interacción o interfaces.

Un patrón resulta ser una solución a un problema. Para que una solución sea considerada patrón debe:
* Comprobar su efectividad resolviendo problemas similares
* Ser reutilizable, lo que significa que es aplicable a diferentes problemas en distintas circunstancias

**¿Por qué usar Patrones en CSS?**
* Construimos sistemas, no páginas
* Necesidad de modularidad
* Mejora flujo de trabajo
* Ya han sido probados y validados
* Si trabajamos en equípo mantiene el órden
* Promueven la filosofía DRY **(Don't Repeat Yourself)**

**[⬆ regresar al índice](#Índice)**


## Frameworks
* [960 Grid System](http://960.gs/)
* [Bootstrap](http://getbootstrap.com/)
* [Foundation](http://foundation.zurb.com/)
* [Skeleton](http://getskeleton.com/)
* [Pure CSS](http://purecss.io/)
* [jQueryMobile](https://jquerymobile.com/)
* [Materialize](http://materializecss.com/)
* [MUI](https://www.muicss.com/)
* [Semantic UI](http://semantic-ui.com/)
* [Flexbox Grid](http://flexboxgrid.com/)
* [Responsimple](http://jonmircha.github.io/responsimple/) :heart_eyes:
* [Comparativas entre Frameworks](http://responsive.vermilion.com/compare.php)

**[⬆ regresar al índice](#Índice)**