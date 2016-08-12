# JavaScript

![JavaScript](http://bextlan.com/img/para-cursos/javascript.jpg)

## "Es el único lenguaje en el que me doy cuenta que las personas sienten que no necesitan aprenderlo antes de empezar a utilizarlo." ([Douglas Crockford](http://www.crockford.com/))

## Índice
1. [JavaScript: BEGINS (1995)](#javascript-begins-1995)
1. [JavaScript: AGE OF FLASH (2000)](#javascript-age-of-flash-2000)
1. [JavaScript: AGE OF HTML5 (2008)](#javascript-age-of-html5-2008)
1. [JavaScript: AGE OF WEB COMPONENTS & REAL TIME (2014)](#javascript-age-of-web-components--real-time-2014)
1. [Librerias y Frameworks](#librerias-y-frameworks)
1. [JavaScript NO es JAVA](#javascript-no-es-java)
1. [EcmaScript](#ecmascript)
1. [Buenas Prácticas](#buenas-prácticas)
1. [Libros](#libros)

### JavaScript: BEGINS (1995)

> JavaScript, conocido como LiveScript, JScript, ECMAScript, es uno de los lenguajes de programación más populares del mundo. Virtualmente cada computadora en el mundo tiene al menos un intérprete Javascript instalado y sin duda es usado frecuentemente (navegador web). La popularidad que tiene Javascript se debe enteramente a su rol como lenguaje de script en la Web.

> A pesar de su popularidad, pocos saben que JavaScript es un lenguaje de programación dinámico, orientado a objetos y de propósito general.

> > [CROCKFORD, Douglas. Javascript: The World’s Most Misunderstood Programming Language, 2001](http://www.crockford.com/javascript/javascript.html)

* Fue creado en 1995 por Brendan Eich de Netscape en **13 días**
* Fue implementado en 1996 en el Nestcape Navigator 2.0 y a partir de ese momento en todos los navegadores
* Todo el mundo puede usarlo sin necesidad de adquirir una licencia
* Es un lenguaje interpretado, es decir, no necesita compilar para ejecutarse
* Se define como orientado a objetos, basado en prototipos
* No es tipado y es dinámico
* Las funciones son objetos de primer órden
* Se utiliza en sitios web para agregar funcionalidad, interactividad validar formularios, comunicarse con el servidor, entre otras cosas
* Es el lenguaje de programación front end de la web

**[⬆ regresar al índice](#Índice)**


### JavaScript: AGE OF FLASH (2000)

* Guerra de los Navegadores
* Se crea [JSON](http://www.json.org/) (_JavaScript Object Notation_) es un formato ligero de intercambio de datos
* Se crea [AJAX](https://es.wikipedia.org/wiki/AJAX) (_Asynchronous JavaScript And XML_), técnica que permite la comunicación asíncrona entre el navegador y el servidor
* Proliferan sitios web hechos en Flash por sobre los hechos en Estándares Web (HTML, CSS y JS)
* [ActionScript](https://es.wikipedia.org/wiki/ActionScript) el lenguaje de Flash evoluciona hasta ser orientado a objetos, su sintaxis es similar a la de JavaScript ya que se basan del mismo estándar [EcmaScript](http://www.ecma-international.org/)
* Proliferan librerías y frameworks para hacer CrossBrowser como [jQuery](https://jquery.com/)

**[⬆ regresar al índice](#Índice)**


### JavaScript: AGE OF HTML5 (2008)

![Implementaciones HTML5](http://www.w3.org/html/logo/badge/html5-badge-h-connectivity-css3-device-graphics-multimedia-performance-semantics-storage.png)
* De 2008 a 2014 se define e implementa [HTML5](https://www.w3.org/html/logo/)
* HTML5 apesta a JavaScript (6 de sus 8 implementaciones son JS)
* Comienzan a proliferar librerías y frameworks para todo propósito
* Comienzan a desarrollarse [API's](https://es.wikipedia.org/wiki/Interfaz_de_programaci%C3%B3n_de_aplicaciones) para la interacción con el software y hardware del usuario a través del navegador
* En 2009 se crea [Node.js ®](https://nodejs.org) el entorno de programación back end de JavaScript
* Comienzan a surgir bases de datos NoSQL basadas en JSON 
* JavaScript comienza a tener una gran [comunidad](https://www.npmjs.com/)

**[⬆ regresar al índice](#Índice)**


### JavaScript: AGE OF WEB COMPONENTS & REAL TIME (2014)

* JavaScript hoy es el único lenguaje capaz de ejecutarse en las 3 capas de una aplicación:
    * Front end (JavaScript)
    * Back end (Node.js)
    * Persistencia de Datos (Varias opciones)

* JavaScript hoy nos permite crear:
    * Sitios Web Front end
    * Aplicaciones SPA (_Single Page Application_)
    * Aplicaciones basadas en Componentes Web
    * Aplicaciones basadas en Microservicios
    * Aplicaciones de Red
    * Aplicaciones Distribuidas y Escalables
    * Aplicaciones en Tiempo Real
    * Aplicaciones Isomórficas (Front end y Back end con el mismo lenguaje de programación)
    * Aplicaciones Híbridas (Nativas)
    * Servidores Web
    * Bases de Datos
    * Scripts para la administración del S.O. desde la terminal de comandos
    * Scripts para la automatización de tareas y pruebas de código
    * Controlar Hardware (Drones)
    * Scripts para la dominación del mundo :earth_americas: :smiling_imp:

**[⬆ regresar al índice](#Índice)**


### Librerias y Frameworks

* Librerías Front end
    * [jQuery](https://jquery.com/)
    * [Modernizr](https://modernizr.com/)
    * [UnderScore](http://underscorejs.org/)
    * [MooTools](http://mootools.net/)
    * [Prototype](http://prototypejs.org/)
* Frameworks Front end
    * [Bootstrap](http://getbootstrap.com/)
    * [Foundation](http://foundation.zurb.com/)
    * [jQueryMobile](https://jquerymobile.com/)
    * [Kendo UI](http://www.telerik.com/kendo-ui)
* Frameworks MV*
    * [Angular](https://angularjs.org/)
    * [Backbone](http://backbonejs.org/)
    * [Ember](http://emberjs.com/)
* Librerías basadas en Componentes Web
    * [React](https://facebook.github.io/react/)
    * [Polymer](https://www.polymer-project.org/)
* Frameworks Back end para [Node](https://nodejs.org/)
    * [Express](http://expressjs.com/)
    * [Socket.IO](http://socket.io/)
    * [Sails](http://sailsjs.org/)
    * [Hapi](http://hapijs.com/)
    * [Koa](http://koajs.com/)
    * [Kraken](http://krakenjs.com/)
* Bases de Datos
    * [MongoDB](https://www.mongodb.org/)
    * [CouchDB](http://couchdb.apache.org/)
    * [RethinkDB](https://www.rethinkdb.com/)
    * [Cassandra](http://cassandra.apache.org/)
    * [Firebase](https://www.firebase.com/)
* Aplicaciones Híbridas (Nativas):
    * [React Native](https://facebook.github.io/react-native/)
    * [Ionic](http://ionicframework.com/)
    * [Meteor](https://www.meteor.com/)
    * [Adobe PhoneGap](http://phonegap.com/)
* Automatización de Tareas
    * [Grunt](http://gruntjs.com/)
    * [Gulp](http://gulpjs.com/)
    * [Webpack](https://webpack.github.io/)
    * [Browserify](http://browserify.org/)
    * [Babel](http://babeljs.io/)
* Gestores de Paquetes
    * [NPM](https://www.npmjs.com/)
    * [Bower](http://bower.io/)
* Linters
    * [JSLint](http://www.jslint.com/)
    * [JSHint](http://jshint.com/)
* Preprocesadores
    * [CoffeeScript](http://coffeescript.org/)
    * [TypeScript](https://www.typescriptlang.org/)

**[⬆ regresar al índice](#Índice)**


### JavaScript NO es JAVA

![This is JS](http://bextlan.com/img/para-cursos/this-is-javascript.jpg)
![JS vs JAVA](http://bextlan.com/img/para-cursos/jsvsjava.jpg)
![JAVA vs JS](http://bextlan.com/img/para-cursos/java-vs-javascript.jpg)

**[⬆ regresar al índice](#Índice)**


### ECMAScript

* ECMAScript es el nombre del estándar internacional que define JavaScript
* Definido por un comité técnico (TC-39) de ecma international.
* Identificado como Ecma-262 y ISO/IEC 16262
* No es parte del W3C
* La versión actual es la ES6 o [ECMAScript 2015](http://www.ecma-international.org/ecma-262/6.0/)

--------------------------------------------------
| Edición | Publicación | Cambios |
| ------- | ----------- | ------- |
| 1 | 1997 |  Primera edición |
| 2 | 1998 |  Cambios editorales para mentener la especificación completa alineada con el estándar internacional ISO/IEC 16262 |
| 3 | 1999 |  Se agregaron expresiones regulares, mejor manejo de strings, nuevo control de declaraciones, manejo de excepciones con try/catch, definición más estricta de errores, formato para la salida numérica y otras mejoras |
| 4 | Abandonado | La cuarta edición fue abandonada debido a diferencias políticas respecto a la complejidad del lenguaje. Muchas características propuestas para la cuarta edición fueron completamente abandonadas; algunas fueron propuestas para la edición ECMAScript Harmony |
| 5 | 2009 | Agrega el modo estricto `strict mode`, un subconjunto destinado a proporcionar una mejor comprobación de errores y evitar constructores propensos a errores. Aclara varias ambigüedades de la tercera edición, y afina el comportamiento de las implementaciones del "mundo real" que difieren consistentemente desde esa especificación. Agrega algunas nuevas características, como getters y setters, librería para el soporte de JSON, y una más completa reflexión sobre las propiedades de los objetos |
| 5.1 | 2011 | Está completamente alineada con la tercera edición del estándar internacional ISO/IEC 16262:2011 |
| 6 | 2015 | La sexta edición agrega cambios significativos en la sintaxis para escribir aplicaciones complejas, incluyendo clases y módulos, definiéndolos sémanticamente en los mismos términos del modo estricto de la edición ECMAScript 5. Otras nuevas características incluyen iteradores for/of loops, generadores y generador de expresiones estilo Python, funciones de dirección, datos binarios, colecciones (mapas, sets, mapas débiles), y proxies (metaprogramación para objetos virtuales y wrappers). Al ser la primera especificación “ECMAScript Harmony”, es también conocida como “ES6 Harmony” |
| 7 |  En progreso | La séptima edición está en una etapa muy temprana de desarrollo, pero está orientada a continuar con la reforma del lenguaje, aislamiento de códigos, control de efectos y librerías/herramientas habilitadas desde ES6. Nuevas características propuestas incluyen promesas/concurrencia, matemáticas y datos numéricos mejorados, guards y trademarks (una alternativa al tipado estático), sobrecarga de operadores, value types (first-class number-like objects), nuevas estructuras de registro (registros, tuplas y vectores tipados), pattern matching, y traits |
--------------------------------------------------

**[⬆ regresar al índice](#Índice)**


### Buenas Prácticas

* [JavaScript The Right Way](http://jstherightway.org/es-es/)
* [JavaScript Garden](http://bonsaiden.github.io/JavaScript-Garden/es/)
* [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript#airbnb-javascript-style-guide-)
* [Can I Use](http://caniuse.com/)
* Compatibilidad [ECMAScript](https://kangax.github.io/compat-table/es6/)
* [La dieta del Navegador](https://browserdiet.com/es/)

**[⬆ regresar al índice](#Índice)**


### Libros

* [Introducción a JavaScript](http://librosweb.es/libro/javascript/)
* [Introducción a AJAX](http://librosweb.es/libro/ajax/)
* [JavaScript The Good Parts](https://www.ebooks-it.net/ebook/javascript-the-good-parts)
* [Eloquent JavaScript](http://eloquentjavascript.net/)

**[⬆ regresar al índice](#Índice)**