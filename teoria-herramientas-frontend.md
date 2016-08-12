# Herramientas Frontend

![Herramientas Frontend](http://bextlan.com/img/para-cursos/herramientas-frontend.jpg)

## Índice

1. [Introducción](link a las slides)
1. [Node.js](#nodejs)
1. [NPM](#npm)
1. [Paquetes NPM](#paquetes-npm)
1. [Git](#git)
1. [GitHub](#github)
1. [Más de Git & GitHub](#más-de-git--github)
1. [Preprocesadores](#preprocesadores)
1. [Gestores de Tareas](#gestores-de-tareas)
1. [Web Performance Optimization]()
	1. https://github.com/davidsonfellipe/awesome-wpo#benchmark---javascript
	1. http://vanessatejada.com/analitica-web/que-es-wpo-web-performance-optimization/
	1. http://pumpun.com/wpo-web-performance-optimization/
	1. https://www.dariobf.com/razones-utilizar-wpo/
	1. https://www.keycdn.com/blog/website-performance-optimization/
1. [Node Version]()
	1. https://frontendlabs.io/3397--node-js-como-trabajar-multiples-versiones-de-node-version-manager

## Node.js

![Node.js](http://bextlan.com/img/para-cursos/nodejs-new-pantone-black.png)

* [nodejs.org](https://nodejs.org/)
* [¿Qué es Node.js?](http://jonmircha.github.io/slides-nodejs/#/7)
* [Modelo Asíncrono y No Bloqueante](http://jonmircha.github.io/slides-nodejs/#/20)
* [Características y Ventajas](http://jonmircha.github.io/slides-nodejs/#/35)
* [io.js y el presente futuro de Node.js](http://jonmircha.github.io/slides-nodejs/#/44)
* [Instalación](http://jonmircha.github.io/slides-nodejs/#/57)
* [Más Info](https://www.youtube.com/playlist?list=PLvq-jIkSeTUY3gY-ptuqkNEXZHsNwlkND)

**[⬆ regresar al índice](#Índice)**


## NPM

![NPM](http://bextlan.com/img/para-cursos/npm-logo.png)

### Node Package Manager

[npmjs.com](https://www.npmjs.com/) es el gestor de paquetes de Node.js... y de todo JavaScript

### Iniciar un proyecto npm

```
$ > npm init //Con asistente
$ > npm init -y //Sin asistente
```

### package.json

* Es el archivo de configuración de un proyecto de node.js
* [Configuración del package.json](http://browsenpm.org/package.json)
* [Semantic Versioning](http://semver.org/)

```json
{
	"name": "module-name",
	"version": "10.3.1",
	"description": "An example module to illustrate the usage of a package.json",
	"author": "Your Name <you.name@example.org>",
	"contributors": [{
		"name": "Foo Bar",
		"email": "foo.bar@example.com"
	}],
	"bin": {
		"module-name": "./bin/module-name"
	},
	"scripts": {
		"test": "vows --spec --isolate",
		"start": "node index.js",
		"predeploy": "echo im about to deploy",
		"postdeploy": "echo ive deployed",
		"prepublish": "coffee --bare --compile --output lib/foo src/foo/*.coffee"
	},
	"main": "lib/foo.js",
	"repository": {
		"type": "git",
		"url": "https://github.com/nodejitsu/browsenpm.org"
	},
	"bugs": {
		"url": "https://github.com/nodejitsu/browsenpm.org/issues"
	},
	"keywords": [
		"nodejitsu",
		"example",
		"browsenpm"
	],
	"dependencies": {
		"primus": "*",
		"async": "~0.8.0",
		"express": "4.2.x",
		"winston": "git://github.com/flatiron/winston#master",
		"bigpipe": "bigpipe/pagelet",
		"plates": "https://github.com/flatiron/plates/tarball/master"
	},
	"devDependencies": {
		"vows": "^0.7.0",
		"assume": "<1.0.0 || >=2.3.1 <2.4.5 || >=2.5.2 <3.0.0",
		"pre-commit": "*"
	},
	"preferGlobal": true,
	"private": true,
	"publishConfig": {
		"registry": "https://your-private-hosted-npm.registry.nodejitsu.com"
	},
	"subdomain": "foobar",
	"analyze": true,
	"license": "MIT"
}
```

**[⬆ regresar al índice](#Índice)**


## Paquetes NPM

### Instalación Única

Se instalan en la carpeta donde se encuentre la terminal de comandos, **NO** se registran en el archivo **`package.json`**

```
$ > npm install [nombre del package]
$ > npm install [nombre del package]@3.4.12 // Versión específica
$ > npm i [nombre del package] //shortcut
```

### Instalación como Dependencia del proyecto

Se instalan en la carpeta donde se encuentre la terminal de comandos, **SI** se registran en el archivo **`package.json`** como dependencias del proyecto, esto significa que el proyecto requiere de éstos paquetes para funcionar

```
$ > npm install [nombre del package] --save
$ > npm install [nombre del package] -S //shortcut
```

### Instalación como Dependencia de Desarrollo del proyecto

Se instalan en la carpeta donde se encuentre la terminal de comandos, **SI** se registran en el archivo **`package.json`** como dependencias de desarrollo del proyecto, esto significa que facilitan y optimizan las tareas comunes de desarrollo y publicación del proyecto

```
$ > npm install [nombre del package] --save-dev
$ > npm install [nombre del package] -D //shortcut
```

### Instalación Global

Se instalan localmente en el ordenador independientemente de donde se encuentre la terminal de comandos, esto significa que estarán disponibles en todas las carpetas del ordenador, **NO** se registran en el archivo **`package.json`**

```
$ > npm install [nombre del package] --global
$ > npm install [nombre del package] -g //shortcut
```

### Instalación Múltiple de paquetes

Se pueden instalar múltiples paquetes, separando sus nombres con un espacio en blanco y al final especificar el flag del tipo de instalación

```
$ > npm install [package1] [package2] [package3] --flag
```

### Instalación de proyecto con `package.json`

Cuando un proyecto tiene el archivo **`package.json`** se pueden instalar todas las dependencias de proyecto y desarrollo que tenga registradas en el mismo.

```
$ > npm install
```

### Actualización de paquetes

```
$ > npm update [package]
```

### Desinstalación de paquetes

Si se utiliza el flag **`--save`** o **`--save-dev`** se elimina el registro del archivo **`package.json`**, si se usa **`--global`** se elimina del ordenador

```
$ > npm uninstall [package] //se borra de la carpeta node_modules
$ > npm uninstall [package] --save
$ > npm uninstall [package] --save-dev
$ > npm uninstall [package] --global
$ > npm un [package] //shortcut
```

### Publicación de paquetes

Un paquete no puede volver a re-publicarse con la misma versión. Si despublicas un paquete puedes romper Internet :grimacing:

```
$ > npm publish
```

### Mostrar información de paquetes

Lee metadatos del archivo **`package.json`** del paquete en su repositorio oficial

```
$ > npm view [package]
$ > npm view [package] versions
```

### [Documentación de NPM](https://docs.npmjs.com/)

**[⬆ regresar al índice](#Índice)**


## Git
![Git](http://bextlan.com/img/para-cursos/logo-git.png)

#### Software de Control de versiones

[Git](https://git-scm.com/) es un software de control de versiones distribuido y descentralizado que permite a un equipo de desarrolladores trabajar sobre el mismo código.

#### Control de versiones distribuido

Se denomina **"distribuido"** porque cada miembro del equipo dispone de una copia completa del código.
![Git es Distribuido](http://bextlan.com/img/para-cursos/git-distributed.png)

#### Control de versiones descentralizado

Los miembros del equipo pueden enviarse código, recibirlo y desarrollar funcionalidades de forma conjunta y separada del servidor central.
![Git es Descentralizado](http://bextlan.com/img/para-cursos/git-centr-decentr.png)

### Ventajas de usar Git

![Estadísticas Git](http://bextlan.com/img/para-cursos/git-estadisticas.png)
* Estándar actual
* Código colaborativo, versionado y distribuido
* Recuperación de archivos
* Mayor control
* Shorcuts y Plugins
* Mejora tu productividad

### Instalación

* [Git](https://git-scm.com/downloads)
* [Source Tree Interfaz Gráfica](https://www.sourcetreeapp.com/)

### Configurando Git por primera vez

```git
$ > git --version
$ > git config --global user.name "Jonathan MirCha"
$ > git config --global user.email jonmircha@gmail.com
$ > git config --global user.ui true
$ > git config --global core.editor nano
$ > git config --list
$ > git help [comando a buscar]
```

### Zonas y Flujo de trabajo básico en Git

#### 1. Directorio de trabajo

Modificas una serie de archivos en tu directorio de trabajo.

![Working Area](http://bextlan.com/img/para-cursos/workingarea.png)

#### 2. Área de preparación

Preparas los archivos, añadiéndolos a tu área de preparación.

![Staging Area](http://bextlan.com/img/para-cursos/stagingarea.png)

#### 3. Repositorio Git

Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación y almacena esa copia instantánea de manera permanente en tu directorio de Git.

![Repositorio](http://bextlan.com/img/para-cursos/repositorio.png)

### Inicializar Git en un directorio local

* **`git init`** crea un directorio oculto **`.git`** donde se almacena toda la información utilizada por git
* El comando UNIX **`touch`** nos crea un nuevo archivo
* En el archivo **`.gitignore`** incluimos todo lo que NO queramos incluir en nuestro repositorio. Lo podemos crear con [gitignore.io](https://www.gitignore.io/)
* **`git status`** nos muestra el listado de archivos nuevos (untracked), borrados o editados

```git
$ > mkdir carpeta
$ > cd carpeta
$ > touch README.md
$ > touch .gitignore
$ > git init
$ > git status
```

### Plataformas web que trabajan con Git

![Git no es GitHub](http://bextlan.com/img/para-cursos/git-github.png)

* [GitHub](https://github.com/)
* [GitLab](https://gitlab.com/)
* [BitBucket](https://bitbucket.org/)
* etc.

### Más Info

* [Git - La guía sencilla](http://rogerdudler.github.io/git-guide/index.es.html)
* [Libro Pro Git](https://git-scm.com/book/es/v2)

**[⬆ regresar al índice](#Índice)**


## GitHub

#### [Crea tu cuenta](https://github.com/)

![GitHub](http://bextlan.com/img/para-cursos/octocat.png)

### Flujo de trabajo básico con Git & GitHub

El flujo se distribuye en tres estados locales y uno remoto

* Estados Locales:
	* **Working Dir:** El directorio donde almacenamos los archivos
	* **Staging:** El estado en el que avisamos a Git de que hemos realizado cambios
	* **HEAD:** El puntero hacia el último bloque de código (commit)
* Estado Remoto:
	* **Remote Origin:** El directorio remoto donde almacenamos los archivos en GitHub

#### Working Dir

El primer nivel es nuestra carpeta de trabajo. Podemos añadir, quitar, editar archivos y Git sólo se encargará de controlar los archivos que han sido modificados.

![Working Dir](http://bextlan.com/img/para-cursos/git-level-wd.png)

Una vez creados, modificados, añadidos o borrados los archivos al **working dir** los pasamos al **staging** mediante:

```git
$ > git add [nombre de archivo(s) o directorio(s)]
$ > git add --all //todos los archivos
$ > git add -A //shortcut todos los archivos
$ > git add . //otro shortcut todos los archivos
```

#### Staging

En el segundo nivel nuestros archivos están preparados para ser empaquetados. Podemos seguir trabajando y repetir el proceso tantas veces como necesitemos.

![Staging](http://bextlan.com/img/para-cursos/git-level-staging.png)

Cuando hemos completado un conjunto de cambios, los "empaquetamos" mediante la instrucción **`commit`** y los colocamos en el **HEAD** mediante:

```git
$ > git commit -m 'mensaje descriptivo'
```

#### HEAD

Nuestro conjunto de cambios está listo para enviar al repositorio remoto. El **HEAD** es nuestra "bandeja de salida". Podemos seguir trabajando y crear más "commits".

![HEAD](http://bextlan.com/img/para-cursos/git-level-head.png)

#### Remote Origin

Ahora vincularemos nuestro repositorio local con uno remoto en Github.

Una vez creado el repositorio remoto en GitHub lo "vinculamos" a nuestro repositorio local mediante:

```git
$ > git remote add origin https://github.com/usuario/repositorio.git
```

Una vez indicando a Git que tenemos un repositorio remoto podemos enviar el conjunto de cambios contenidos en nuestro **HEAD**. Por defecto Git denomina **origin** a nuestro repositorio remoto y crea una rama llamada **master** mediante:

```git
$ > git push -u origin master //la primera vez que vinculamos el repositorio remoto con el local
$ > git push //para las subsecuentes actualizaciones
```

![Remote Origin](http://bextlan.com/img/para-cursos/git-level-origin-master.png)

#### Sincronizando versiones

Antes de enviar nuestros cambios tenemos que bajarnos la última versión del repositorio remoto, obtenemos los últimos cambios de **origin** y los combinamos con la rama **master**

Cuando obtenemos archivos del repositorio remoto a nuestra copia local Git obtiene todos los archivos nuevos que se hayan añadido y elimina los que se hayan quitado.

```git
$ > git pull -u origin master //la primera vez que descargamos el repositorio remoto al local
$ > git pull //para las subsecuentes actualizaciones
```

![Git Pull](http://bextlan.com/img/para-cursos/git-level-pull.png)

#### Revisando el Historial

**`git log`** nos permite conocer todo el historial de un proyecto, con la información de la fecha, el autor y id de cada cambio

```git
$ > git log
$ > git log --oneline
$ > git log > commits.txt
```

### Más Info

* [Guías Oficiales de GitHub](https://guides.github.com/)
* [Try GitHub](https://try.github.io)

**[⬆ regresar al índice](#Índice)**


## Más de Git & GitHub

### Ramas

Una rama nos permite aislar una nueva funcionalidad en nuestro código que después podremos añadir a la versión principal.

```git
$ > git branch [nombre-rama] //crear rama
$ > git branch -d [nombre-rama] //eliminar rama
$ > git branch -D [nombre-rama] //eliminar rama (forzado)
$ > git branch //listar ramas
```

### Moverse en el Historial

Podemos desplazarnos en el historial del proyecto hacia atrás o adelante en cambios o ramas , sin afectar el proyecto como tal.

```git
$ > git checkout [nombre-rama] //cambiar a una rama
$ > git checkout [id-commit] //cambiar a un cambio
```

### Resetear

Podemos eliminar el historial de cambios del proyecto hacia adelante con respecto de un punto de referencia.

```git
$ > git reset --soft //borra el HEAD
$ > git reset --mixed //borra el HEAD y el Staging
$ > git reset --hard //borra el HEAD, Staging y WorkingDir
```

### Fusiones

Une dos ramas. Para hacer una fusión necesitamos:

1. Situarnos en la rama que se quedará con el contenido fusionado.
1. Fusionar

Cuando se fusionan ramas se pueden dar 2 resultados diferentes:

* **Fast-Forward**: La fusión se hace automática, no hay conflictos por resolver
* **Manual Merge**: La fusión hay que hacerla manual, para resolver conflictos de duplicación de contenido

```git
$ > git checkout [rama-principal] //Nos cambiamos a la rama principal que quedará de la fusión
$ > git merge [rama-secundaria] //Ejecutamos el comando merge con la rama secundaria a fusionar
```

### Etiquetas

Con esta opción git nos permite versionar nuestro código, librería o proyecto

```git
$ > git tag [numero-versión] //crear una etiqueta
$ > git show [numero-versión] //mostrar información de una etiqueta
$ > git tag //listar etiquetas

$ > git add .
$ > git commit -m 'v1.0.0'

$ > git push origin [numero-versión] //compartir etiqueta en GitHub
```

### Clonar repositorios

```git
$ > git clone [url-repositorio]
```

### GitHub Pages

[**`gh-pages`**](https://pages.github.com/) es una rama especial para crear un sitio web a tu proyecto alojado directamente en tu repositorio de Github.

* URL del repositorio: **https://github.com/usuario/repositorio**
* URL del sitio: **https://usuario.github.io/repositorio**

```git
$ > git init
$ > git add .
$ > git commit -m 'Creando sitio web en GitHub Pages'

$ > git branch gh-pages
$ > git checkout gh-pages

$ > git remote add origin https://github.com/usuario/repositorio.git
$ > git push origin gh-pages

$ > git pull origin gh-pages
```

**[⬆ regresar al índice](#Índice)**


## Preprocesadores

![Preprocesadores](http://bextlan.com/img/para-cursos/preprocesadores.png)

Son lenguajes independientes (generalmente, más amigables, potentes y prácticos) que son capaces de traducir el código al lenguaje de destino (HTML, CSS o JavaScript), que son los únicos que los navegadores son capaces de entender de forma nativa.

El objetivo de los preprocesadores es tener un código más sencillo de mantener y editar. Incluyen características tales como variables, funciones, mixins, anidación y modularidad.

Son soportados por plataformas web como:

* [CodePen](http://codepen.io/)
* [JSFiddle](https://jsfiddle.net/)
* [JS Bin](http://jsbin.com/)

### Preprocesadores HTML

* Markdown
	* [¿Qué es?](http://whatismarkdown.com/)
	* [Guía](http://joedicastro.com/pages/markdown.html)
	* [Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
	* [Tutorial interactivo](http://www.markdowntutorial.com/)
	* [Dillinger - md en vivo](http://dillinger.io/)
	* [Hashify  - md en vivo](http://hashify.me/)
* [Jade](http://jade-lang.com/)
* [Haml](http://haml.info/)
* [Slim](http://slim-lang.com/)
* [Handlebars](http://handlebarsjs.com/)
* [EJS](http://ejs.co/)

### Preprocesadores CSS

* [Less](http://lesscss.org/)
* [Stylus](http://stylus-lang.com/)
* [Sass](http://sass-lang.com/)
	* Sintaxis Sass
	* Sintaxis SCSS
* [PostCSS](http://postcss.org/)
	* [CSSNext](http://cssnext.io/)

### Preprocesadores JS

* [LiveScript](http://livescript.net/)
* [CoffeeScript](http://coffeescript.org/)
* [TypeScript](https://www.typescriptlang.org/)
* [Babel](http://babeljs.io/)

**[⬆ regresar al índice](#Índice)**


## Gestores de Tareas

![Gestores de Tareas](http://bextlan.com/img/para-cursos/build-systems-task-runners.png)

También llamados **Build Systems** o **Task Runners**, permiten automatizar tareas comunes de desarrollo, tales como la minificación de código, recarga del navegador, compresión de imágenes, validación de sintaxis de código, compilación de preprocesadores y un sin fin de tareas más.

No importa si eres un desarrollador Frontend o Backend. Si hoy en día no quieres perder tiempo realizando tareas comunes manualmente, debes usarlos. Estos gestores de tareas se ayudan de componentes (plugins) para llevar a cabo su labor y cada uno tiene su propia manera de configurarse, usa el que más se acomode a tu filosofía de trabajo :grinning:.

* [Grunt](http://gruntjs.com/)
* [Gulp](http://gulpjs.com/)
* [Brunch](http://brunch.io/)
* [Webpack](https://webpack.github.io/)
* [Comandos NPM](https://docs.npmjs.com/)

**[⬆ regresar al índice](#Índice)**