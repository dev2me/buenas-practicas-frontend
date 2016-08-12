# Responsive Web Design
![Responsive Web Design](http://bextlan.com/img/para-cursos/responsive-design.jpg)

## Índice
1. [Traducciones al español](#traducciones-al-español)
1. [Un poco de historia](#un-poco-de-historia)
1. [Concepto](#concepto)
1. [Técnicas de Diseño Web MultiDispositivo](#técnicas-de-diseño-web-multidispositivo)
1. [Enfoques de Diseño Web MultiDispositivo](#enfoques-de-diseño-web-multidispositivo)
1. [Media Queries](#media-queries)
1. [Breakpoints](#breakpoints)
1. [Más Recursos](#más-recursos)


## Traducciones al español:
* Diseño Web Sensible o
* Diseño Web Adaptable o
* Diseño Web Responsivo o
* etc.

**[⬆ regresar al índice](#Índice)**


## Un poco de historia
 -----------------------------------------------------------------------------------------
| En 2007...                                                                              |
| --------------------------------------------------------------------------------------- |
| ![2007: Hola iPhone](http://bextlan.com/img/para-cursos/steve-iphone.png)               |
| ![Estadísticas de Resolución 1024x768](http://bextlan.com/img/para-cursos/1024x768.png) |
| ![This is not the web](http://bextlan.com/img/para-cursos/not-the-web.png)              |
| ![This is the web](http://bextlan.com/img/para-cursos/this-is-the-web.png)              |
| ![This will be there](http://bextlan.com/img/para-cursos/will-be-the-web.png)           |
 -----------------------------------------------------------------------------------------

Tanto la idea como el propósito del Responsive Web Design fueron previamente discutidos y descritos por la [W3C](https://www.w3.org/) el 29 de julio de 2008 en su recomendación "[Mobile Web Best Practices](https://www.w3.org/TR/mobile-bp/)"

Dicha recomendación, aunque específica para dispositivos móviles, puntualiza que está hecha en el contexto de **una única web** ([One Web](https://www.w3.org/TR/mobile-bp/#OneWeb)), y que por lo tanto engloba no solo la experiencia de navegación en dispositivos móviles sino también en dispositivos de mayor resolución de pantalla como dispositivos de escritorio

El concepto de **One Web** hace referencia a la idea de construir una web para todos (**Web for All**) y accesible desde cualquier tipo de dispositivo (**Web on Everything**)

**[⬆ regresar al índice](#Índice)**


## Concepto 
### En 2010 - 2011
Formalmente **Responsive Web Design** fue un término acuñado el 25 de mayo de 2010 por [Ethan Marcotte](https://twitter.com/beep) en su artículo [Responsive Web Design](http://alistapart.com/article/responsive-web-design) publicado en [A List Apart](http://alistapart.com/about) y posteriormente argumentado en el [libro de mismo nombre](https://abookapart.com/products/responsive-web-design) publicado en 2011.

En dichas fechas (2010-2011) se presenta como una filosofía de diseño y desarrollo cuyo objetivo es adaptar la apariencia de los sitios y aplicaciones web al dispositivo que se esté utilizando para visualizarlos.

Se basa en 3 principios de CSS:

1. Maquetación Fluída
2. Multimedios Flexibles
3. Uso de Media Queries

### HOY
Hoy día los sitios y aplicaciones web se visualizan en multitud de tipos de dispositivos como:
* Tabletas
* Teléfonos inteligentes
* Lectores electrónicos, 
* Portátiles
* Equipos de Escritorio
* Relojes
* Pantallas
* etc

Además, cada tipo de dispositivo tiene sus características concretas:
* Tamaño de pantalla
* Resolución
* Potencia de CPU
* Capacidad de memoria
* etc

Por tales motivos el Responsive Web Design hoy:
* No se trata exclusivamente de reacomodar la información
* Sino de entregar el contenido de manera óptima, considerando las características de hardware, software y tipos de conexiones, del dispositivo que el usuario este usando

___

### Hoy Responsive Web Design es la manera de hacer Diseño Web Actual para MultiDispositivos
___

**[⬆ regresar al índice](#Índice)**


## Técnicas de Diseño Web MultiDispositivo
* [Responsive Web Design](https://abookapart.com/products/responsive-web-design) (CSS)
* [Adaptive Web Design](http://adaptivewebdesign.info/) (Diferentes versiones del sitio)
* [Responsible Responsive Design](https://abookapart.com/products/responsible-responsive-design) (CSS + JS)
* [RESS](http://www.lukew.com/ff/entry.asp?1392) (Responsive Web Design + Server Side)
* [AMP](https://www.ampproject.org/) (Accelerated Mobile Pages)

**[⬆ regresar al índice](#Índice)**


## Enfoques de Diseño Web MultiDispositivo

 ---------------------------------------
| Enfoque | Mobile First | Desktop First |
| --------| ------------ | ------------- |
| Técnica | Progressive Enhancement | Graceful Degradation |
| CSS General | Equipo Móvil | Equipo de Escritorio |
| Media Queries | min-width | max-width |
| Breakpoints | Del Menor al Mayor | Del Mayor al Menor |
| | ![Mobile First](http://bextlan.com/img/para-cursos/mobile-first.png) | ![Desktop First](http://bextlan.com/img/para-cursos/desktop-first.png) |
 ---------------------------------------

**[⬆ regresar al índice](#Índice)**


## Media Queries
Desde la especificación de CSS 2.1, las hojas de estilo han tenido cierto grado de capacidad para el reconocimiento de dispositivos mediante el uso de tipos de medios. Por ejemplo:

```html
<link rel="stylesheet" href="print.css" media="print">
```

Con CSS3, la W3C perfeccionó y mejoró los tipos de medios con características multimedia y con la capacidad de preguntar dichas características a los medios

Esto no sólo hace posible inspeccionar el contenido que se entrega al dispositivo, sino también las características físicas reales del dispositivo

El uso de media queries permite pedir fácilmente al navegador sus características, tales como anchura, altura, relación de aspecto y la orientación

La sintaxis es la siguiente:

```css         
@media screen and (max-width:480px) and (orientation:portrait) {
    /* 
    Código CSS que se aplicará cuando se cumpla la media queries
    */
}
```

* [¿Puedo usarlas?](http://caniuse.com/#search=css3%20media)
* Inspírate en [mediaqueri.es](http://mediaqueri.es/)
* Lista completa de [media queries](https://www.w3.org/TR/css3-mediaqueries/)

**[⬆ regresar al índice](#Índice)**


## Breakpoints
Ethan Marcotte en su libro Responsive Design (113-114 pags) nos propone la siguiente lista de puntos de interrupción según la resolución del dispositivo:

 ---------------------------------------
| Tamaño  | Dispositivos |
| ------- | ------------ |
| 320px   | Para dispositivos con pantallas pequeñas, como los teléfonos en modo vertical |
| 480px   | Para dispositivos con pantallas pequeñas, como los teléfonos, en modo horizontal |
| 600px   | Tabletas pequeñas, como el Amazon Kindle (600×800) y Barnes & Noble Nook (600×1024), en modo vertical |
| 768px   | Tabletas de diez pulgadas como el iPad (768×1024), en modo vertical |
| 1024px  | Tabletas como el iPad (1024×768), en modo horizontal, así como algunas pantallas de ordenador portátil, netbook, y de escritorio |
| 1200px  | Para pantallas panorámicas, principalmente portátiles y de escritorio |
 ---------------------------------------

### Importante... Convierte tus Breakpoints a EMs

#### ¿Por qué?

Aunque los pixeles se consideran una unidad de medida absoluta, en realidad son unidades relativas a la resolución de pantalla del dispositivo que lo visualiza, si dicho dispositivo tiene una densidad mayor a la normal, entonces la proporción de los pixeles cambiará, por ello es importante que los breakpoints de las media queries se conviertan a ems que si son unidades relativas y proporcionales

* [The EMs have it: Proportional Media Queries](http://blog.cloudfour.com/the-ems-have-it-proportional-media-queries-ftw/)
* [Why Ems?](https://css-tricks.com/why-ems/)
* [CSS px is an Angular Measurement](http://inamidst.com/stuff/notes/csspx)

#### Fórmula de conversión

---------------------------------------
| Objetivo en pixeles / Contexto en pixeles = Resultado en Ems |
| -------- |
| 320px / 16px = 20em |
| 480px / 16px = 30em |
| 600px / 16px = 37.5em |
| 768px / 16px = 48em |
| 1024px / 16px = 64em |
| 1200px / 16px = 75em |
---------------------------------------

**[⬆ regresar al índice](#Índice)**


## Más Recursos
* [ResponsiveDesign.is](https://responsivedesign.is/)
* [Responsive Resources](http://bradfrost.github.io/this-is-responsive/resources.html)
* [Responsive Patterns](http://bradfrost.github.io/this-is-responsive/patterns.html)
* [Guía para Móviles de Google](https://developers.google.com/webmasters/mobile-sites/?hl=es)
* [SEO para Móviles de Google](https://developers.google.com/webmasters/mobile-sites/mobile-seo/?hl=es)
* [Prueba de optimización para móviles de Google](https://www.google.com/webmasters/tools/mobile-friendly/)
* [PageSpeed Insights de Google](https://developers.google.com/speed/pagespeed/insights/)

**[⬆ regresar al índice](#Índice)**