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
		<li>500ml de acite</li>
		<li>Veneno mortal</li>
	</ul>
</body>
</html>
```

## Como se puede incluir javascript en HTML.

### Introducir JavaScript en los elementos de HTML
Esta es la forma menos utilizada, consiste precisamente en introducir los elementos de JavaSript en una etiqueta de nuestro código html, un ejemplo sería "<span onclick="alert('Hola Mundo!')">Haz click aquí</span>", el problema que tiene este método es que ensucia mucho el código HTML y complica su mantenimiento.

### Introducir JavaScript en el documento
Seguimos introduciendo el código dentro del mismo documento solo que esta vez lo hacemos entre las etiquetas <script> que se pueden introducir en cualquier parte del código html, aunque es recomendable que se haga dentro de la cabecera del documento XHTML, es decir dentro de la etiqueta <head>. 
Ejemplo:
	
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

Para que el documento quede validado la etiqueta script debe de tener el atributo type=”text/javascript”.

### Introducir JavaScript en un archivo externo
La mejor opción cuando tenemos un código que afecta a diferentes páginas del sitio o es un código muy elaborado.

Para ello utilizamos de nuevo la etiqueta script que podemos repetir para insertar diferentes archivos JS en un mismo sitio por medio del atributo src que apunta la url del archivo JS que se quiere enlazar. Estos archivos cuya extensión es .js se pueden crear con cualquier editor de texto que queramos.
