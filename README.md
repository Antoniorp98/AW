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
```html
### Definir CSS en un archivo externo

Los estilos se incluyen en un archivo con extensión .css que las páginas HTML enlazan mediante la etiqueta <link>. Los atributos que deben incluir son:

- rel: indica el tipo de relación que tiene el recurso enlazado y la página HTML. En CSS, se usa stylesheet.
- type: indica el tipo de recurso enlazado. En CSS, es text/css.
- href: indica la URL del archivo CSS que contiene los estilos. La URL puede ser relativa o absoluta.
- media: indica el medio en el que se van a aplicar los estilos del archivo CSS. En principio, para este ejemplo no es importante, lo normal es poner all.

### Incluir CSS en los elementos HTML

Se utiliza la etiqueta <style> como atributo de la etiqueta que queremos personalizar.
	
### incluir CSS en el propio documento HTML

Mediante la etiqueta <style> dentro de la cabecera del documento. Dentro de <style> ponemos los estilos que queramos incluir en el documento HTML. Es importante incluir el atributo type=”text/css”.

Es usado para definir estilos especificos en una determinada página HTML. Su desventaja es a la hora de modificar los estilos, ya que debemos cambiar los estilos de todas las páginas donde lo hayamos incluido de esta manera.
```
