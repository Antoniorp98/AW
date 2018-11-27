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

<p>Ingredientes</p>
<ul>
  <li>2 huevos</li>
  <li>500g de arina</li>
  <li>1 cucharada de sal</li>
  <li>500ml de aceite<li>
  <li>Veneno mortal<li>
</ul>

</body>
</html>

