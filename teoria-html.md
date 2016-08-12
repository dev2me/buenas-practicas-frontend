# HTML Hyper Text Markup Language
**(Lenguaje de Marcado de Hiper Texto)**

![HTML](http://bextlan.com/img/para-cursos/html5-logo.png)

## Índice
1. [Estructura y Contenido](#estructura-y-contenido)
1. [Etiquetas HTML](#etiquetas-html)
1. [Semántica](#semántica)
1. [Buenas Prácticas de Código HTML](#buenas-prácticas-de-código-html)
1. [Estructura Básica HTML5](#estructura-básica-html5)
1. [Más Info](#más-info)


## Estructura y Contenido

* Lenguaje de marcado basado en etiquetas y atributos, nos define estructura y contenido
* El contenido es el Rey
* Planear bien nuestra estructura de HTML (uso de etiquetas)
* Trabajar la semántica
* La semántica de nuestras etiquetas la define el contenido y su distribución
* Los motores de búsqueda son ciegos, si tu contenido esta bien estructurado, tu contenido será bien posicionado

**[⬆ regresar al índice](#Índice)**


## Etiquetas HTML

[Tabla periódica de las etiquetas HTML](http://zqsmm.qiniucdn.com/data/20110511083224/index.html)
![Tabla de las Etiquetas de HTML](http://bextlan.com/img/para-cursos/periodic-table.png)

**[⬆ regresar al índice](#Índice)**


## Semántica

La semántica es sólo una de las 8 implementaciones de [HTML5](https://www.w3.org/html/logo/)

Con las etiquetas semánticas mejoramos la definición de nuestro contenido, es más entendible tanto para humanos como para máquinas(algoritmos de buscadores)

Recuerda que las etiquetas semánticas no tienen una posición fija en el layout, quien determina la estructura es el contenido

### Etiquetas semánticas y estructurales

* **`<section>`**: Contenido genérico estructurado
* **`<article>`**: Contenido estructural distribuible de manera independiente
* **`<aside>`**: Contenido secundario relacionado o que acompaña o complementa a otro
* **`<header>`**: Contenido introductorio suele tener elementos de navegación y encabezados (h1...h6)
* **`<footer>`**: Sección que contiene información acerca del documento o página
* **`<nav>`**: Sección relativa a enlaces dentro del documento o página
* **`<main>`**: Contenido principal
* **`<figure>`**: Sección de contenido visual, múltiples medios
* **`<figcaption>`**: Leyenda o pié relativo al contenido visual de FIGURE, uno FIGCAPTION por cada FIGURE, puede contener semántica

### Ejemplo de semántica HTML5

![Semántica HTML5](http://bextlan.com/img/para-cursos/semantic-html5.jpg)

**[⬆ regresar al índice](#Índice)**


## Buenas Prácticas de Código HTML

### Especificar

* Tipo de documento HTML5
* Atributo de idioma
* Juego de caractéres
* Area de Visualización
    
### Definir

* Título único máx 65 caractéres
* Descripción única máx 156 caractéres
* Estilos antes de `</head>`
* Scripts antes de `</body>`
* **NO** Cerrar etiquetas únicas así **`<img src=" ">`** en vez de **`<img src=" "/>`**
* Definir atributos booleanos así **`<input type="button" disabled>`** en vez de **`<input type="button" disabled="disabled">`**
* Definir atributos en el siguiente orden:
	* class (si se tiene más de una clase separar con 2 espacios)
	* id, name
    * data-*
    * src, for, type, href, value
    * title, alt
    * aria-*, role

**[⬆ regresar al índice](#Índice)**


## Estructura Básica HTML5
```HTML
<!DOCTYPE html>
<html lang="es">
<head>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<meta charset="UTF-8">
	<title>Título de mi documento, este deberá ser único max 65 caracteres</title>
	<meta name="description" content="Breve descripción de lo que los usuarios 
	encontrarán en este documento, deberá ser única max 156 caracteres">
	<link rel="stylesheet" href="estilos.css">
</head>
<body>
	<h1>Estructura de Documento HTML5</h1>
	<!-- 
		AQUÍ EL CONTENIDO HTML
		Esto es un comentaerio HTML
	-->
	<script src="codigos.js"></script>
</body>
</html>
```

**[⬆ regresar al índice](#Índice)**


## Más Info
* [Guía de Referencia HTML en MDN](https://developer.mozilla.org/es/docs/Web/HTML)
* [Introducción a HTML](http://librosweb.es/libro/xhtml/)
* [Guía de Buenas Prácticas en Código Front end](http://mdo.github.io/code-guide/)
* [La dieta del Navegador](https://browserdiet.com/es/)
* [Can I Use](http://caniuse.com/)

**[⬆ regresar al índice](#Índice)**