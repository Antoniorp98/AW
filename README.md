# Ejercicios HTML y CSS
## Estructura mínima de una web.
```html
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>

</body>
</html>
```

## Explica las 3 formas de usar CSS en HTML.

### Definir CSS en un archivo externo

Los estilos se incluyen en un archivo con extensión .css que las páginas HTML enlazan mediante la etiqueta <link>. Los atributos que deben incluir son:

- rel: indica el tipo de relación que tiene el recurso enlazado y la página HTML. En CSS, se usa stylesheet.
- type: indica el tipo de recurso enlazado. En CSS, es text/css.
- href: indica la URL del archivo CSS que contiene los estilos. La URL puede ser relativa o absoluta.
- media: indica el medio en el que se van a aplicar los estilos del archivo CSS. En principio, para este ejemplo no es importante, lo normal es poner all.

### Incluir CSS en los elementos HTML

Se utiliza la etiqueta <style> como atributo de la etiqueta que queremos personalizar.
	
### Incluir CSS en el propio documento HTML

Mediante la etiqueta <style> dentro de la cabecera del documento. Dentro de <style> ponemos los estilos que queramos incluir en el documento HTML. Es importante incluir el atributo type=”text/css”.

Es usado para definir estilos especificos en una determinada página HTML. Su desventaja es a la hora de modificar los estilos, ya que debemos cambiar los estilos de todas las páginas donde lo hayamos incluido de esta manera.

## Crea una lista sin ordenar con 5 ingredientes de una receta de cocina.
```html
<!DOCTYPE html>
<html>
<head>
<style>
ul {
    list-style-type: square;
}
</style>
</head>
<body>
	<p>Ingredientes:</p>
	<ul>
		<li>1 cucharada de sal</li>
		<li>500g de harina</li>
		<li>2 huevos</li>
		<li>500ml de aceite</li>
		<li>Veneno mortal</li>
	</ul>
</body>
</html>
```

## Como se puede incluir javascript en HTML.

### Introducir JavaScript en los elementos de HTML
Esta es la forma menos utilizada, consiste precisamente en introducir los elementos de JavaSript en una etiqueta de nuestro código html, un ejemplo sería ```<span onclick="alert('Hola Mundo!')">Haz click aquí</span>```, el problema que tiene este método es que ensucia mucho el código HTML y complica su mantenimiento.

### Introducir JavaScript en el documento
Seguimos introduciendo el código dentro del mismo documento solo que esta vez lo hacemos entre las etiquetas <script> que se pueden introducir en cualquier parte del código html, aunque es recomendable que se haga dentro de la cabecera del documento XHTML, es decir dentro de la etiqueta <head>. 
Ejemplo:
```html	
<html>
<head>
    <title>Introducción de código js en las etiquetas script</title>
    <script type="text/javascript">
        alert('Hola Mundo!');
    </script>
</head>
<body>
Bienvenido a JavaScript
</body>
</html>
```
Para que el documento quede validado la etiqueta script debe de tener el atributo type=”text/javascript”.

### Introducir JavaScript en un archivo externo
La mejor opción cuando tenemos un código que afecta a diferentes páginas del sitio o es un código muy elaborado.

Para ello utilizamos de nuevo la etiqueta script que podemos repetir para insertar diferentes archivos JS en un mismo sitio por medio del atributo src que apunta la url del archivo JS que se quiere enlazar. Estos archivos cuya extensión es .js se pueden crear con cualquier editor de texto que queramos.

Archivo script.js

```alert('Hola Mundo!');```

Archivo html que enlaza a script.js
```html
<html>
<head>
    <title>Introducción de código js en las etiquetas script</title>
    <script type="text/javascript" src="script.js"></script>
</head>
<body>
Bienvenido a JavaScript
</body>
</html>
```
Esta forma simplifica el código de la pagina ya que no tiene elementos extraños, se puede reutilizar en todas las páginas del sitio, es fácil de mantener y modificar para que afecte a todas las webs del sitio, por lo que es la más recomendable de utilizar.

## ¿Que diferencia hay entre una clase y una ID?

Dentro de los selectores en CSS, cada uno tiene un determinado peso siendo el Selector de Id el que tiene más peso, seguido del selector de Clase y finalmente el selector de tipo. Dd se usa par aidentificar un elemento unico en el documento HTML, eso significa que si hay un elemento que tiene asignado el atributo ID="principal" no podrá haber otro ID con igual valor (es decir, con el mismo nombre).Para su sintaxis, solamente se utiliza el carácter (#) delante de la id a la que vayamos a modificar sus parámetros, mientras que las clases (class) se usan para aplicar estilos iguales a varios elementos HTML, o sea, una clase es una serie de estilos definidos que se pueden usar muchas veces en cualquier etiqueta HTML. El selector de clases consta de un punto (.) seguido por el nombre de la clase que hayamos creado (el nombre lo elegimos nosotros).


## Código para hacer un enlace a otra página y que esta se abra en una nueva ventana.

```html
<!DOCTYPE html>
<html>
<body>
<a href="https://animeflv.net/" target="_blank">Anime</a>
</body>
</html>
```

## ¿Qué son las pseudoclases? Pon ejemplos.

Las pseudoclases, junto con los pseudoelementos, permiten aplicar un estilo a un elemento no sólo en relación con el contenido del árbol de documento, sino también en relación a factores externos como el historial del navegador, el estado de su contenido, o la posición del ratón.
Ejemplos:
- :left
- :right
- :not()
- :active

## Explica el modelo de caja de CSS (margin, border y padding)

La caja de CSS tiene como principales atributos el margin, border y padding, el margin es la distancia del borde de un elemento hacia otro, el border define el grosor del borde y el padding es la distancia desde el borde hasta el contenido.

## Explica que son los selectores de CSS y pon ejemplos

Se utilizan para seleccionar los elementos HTML a los que les queremos editar el estilo, algunos ejemplos serían:

- Selector de tipo o etiqueta: Selecciona todos los elementos que que coincidan en la etiqueta HTML.

- Selector descendente: Selecciona elementos que se encuentren dentro de otros.

- Selector universal: Selecciona todos los elementos de la página.

## Di a quien afectan:
```html
p a { color: red;	Afectaría a todos los elementos "a" que desciencan de "p".
p > a { color: red; }	Afectaría a todos los elementos "a" que sean hijos inmediatos de "p".
h1 + h2 { color: red }	Afectaría a los elementos "h2" que sean seguidores inmediatos de "h1".
a[class] { color: blue; }	Afectaría a todos los elementos "a" con el atributo "class".
a[class="externo"] { color: blue; }	Afectaría a todos los elementos "a" con una clase de valor "externo".
a[href="http://www.ejemplo.com"] { color: blue; }	Afectaría a todos los elementos "a" con el elemento "href" que contenga el link "http://www.ejemplo.com".
```
