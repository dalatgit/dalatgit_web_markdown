# Accesibilidad HTML
Aquí encontrarás ejemplos de como aplicar accesibilidad en HTML

## Estructura básica de HTML
Por favor indica el idioma y la codificación UTF-8 al momento de establecer la base HTML sobre la cual vas a construir tu sitio web. La codificación UTF8 ayuda a mostrar correctamente caracteres especiales como acentos y ñ en una página web.

```html
<html lang="es">
   <head> <!–– estilos, metatags, scrips ––>
      <title>Título</title>
      <meta charset="UTF-8">
   </head>
   <body>
      <h1>Encabezado principal</h1>
      <p>Cuerpo</p>
   </body>
</html>
```

## Cabeceras
Los encabezados se deben utilizar como título de distintos niveles para que el lector de pantalla pueda interpretar la importancia de los contenidos. Por ejemplo: nivel 1, encabezado 1. Nivel 2, encabezado 2. Se debe utilizar solo un encabezado h1 por página. No se deben utilizar para darle formato al texto, es decir, es una mala práctica utilizar los encabezados para poner un texto más grande que otro.

```html
<h1>Encabezado principal</h1>

<h2>Encabezado secundario 1</h2>
<h3>subtítulo uno</h3>

<h2>Encabezado secundario 2</h2>
<h3>subtítulo dos</h3>
```

## Agregar texto alternativo en imágenes
Podemos utilizar la etiqueta <alt> para añadir un texto alternativo a las imágenes, el cual debe ser una descripción de la misma.
Esto también sirve, no solo para utilizarse con el lector de pantalla, sino en el caso de por ejemplo conexiones lentas, dicha descripción aparecerá cuando las imágenes no se cargan. Las imágenes decorativas no necesitan texto alternativo (pues no le dan contexto a la página) y deben tener alt=”” (alt vacío, no eliminar el atributo alt).

<a href="http://www.freeimages.co.uk/galleries/workplace/education/slides/computer_learning.htm" target="_blank"><img src="http://www.freeimageslive.com/galleries/workplace/education/preview/computer_learning.jpg" title="Foto de manzana verde sobre una computadora portátil del sitio web www.freeimages.co.uk" alt="Foto de manzana verde sobre una computadora portátil del sitio web www.freeimages.co.uk" width="400" height="266" /></a><br/>

Créditos de la imagen: [Sitio web de imágenes gratuitas FreeImages](http://www.freeimages.co.uk/){target=_blank}

```html
<a href="http://www.freeimages.co.uk/galleries/workplace/education/slides/computer_learning.htm" target="_blank"><img src="http://www.freeimageslive.com/galleries/workplace/education/preview/computer_learning.jpg" title="Foto de manzana verde sobre una computadora portátil del sitio web www.freeimages.co.uk" alt="Foto de manzana verde sobre una computadora portátil del sitio web www.freeimages.co.uk" width="400" height="266" /></a><br/>
```

Nota: la descripción de la imagen debe ir acorde con el contexto de la información presentada en la web. Ejemplo: si la web es de un negocio de hoteles y se incluye una foto de la parte frontal del hotel, que además incluye autos y personas caminando y un helicóptero que justo pasaba por ese momento junto al hotel es suficiente con indicar en el texto alternativo algo como “Imagen del edificio del hotel en la avenida ABC ciudad de DEF”

## Enlaces
Los enlaces son interpretados por los lectores de pantalla, como lo que son, vínculos a otros sitios o dentro del mismo sitio y el nombre del enlace debe indicar claramente a que se refiere y describir el contenido al que se va a redirigir al usuario. No usar enlaces llamados "click aquí" o "ir a sitio". No se deben crear enlaces que no vinculen contenido con el fin de dar formato al texto.

[Buscador google](http://www.google.com)

```html
<a href=”http://www.google.com”>Buscador google</a>
```

## Listados
Utiliza las etiquetas html adecuadas tanto para listas ordenadas y desordenadas. De esta forma le damos sentido semántico a la lista.

Lista desordenada:

<ul>
   <li>Azul</li>
   <li>Rojo</li>
   <li>Verde</li>
</ul>

```html
<ul>
   <li>Azul</li>
   <li>Rojo</li>
   <li>Verde</li>
</ul>
```

Lista ordenada:

<ol>
   <li>Primero</li>
   <li>Segundo</li>
   <li>Tercero</li>
</ol>

```html
<ol>
   <li>Primero</li>
   <li>Segundo</li>
   <li>Tercero</li>
</ol>
```

## Formularios
Los formularios web deben tener una etiqueta que describa correctamente la función del formulario. El lector de pantalla lee la etiqueta identificatoria. Los controles deben tener la etiqueta <label>. Se utiliza la etiqueta <fieldset> si agrupo elementos. Se deben indicar los errores de forma correcta. Agregar instrucciones sobre cómo completar el formulario, por ejemplo al completar la contraseña qué características debe cumplir.

<form>  
<label for="correo">Email:</label>
<input id="correo" name="correo" type=email aria-required="true">

<label for="password1">Password:</label>
<input id="password1" name="password1" type=password aria-required="true">

<input type="submit" value="Ingresar">
</form>

```html
<form>  
<label for="correo">Email:</label>
<input id="correo" name="correo" type=email aria-required="true">

<label for="password1">Password:</label>
<input id="password1" name="password1" type=password aria-required="true">

<input type="submit" value="Ingresar">
</form>
```

## Tablas
- Antes de pensar en etiquetas y atributos html, responde estas preguntas: Realmente necesito una tabla? Puedo reducir el número de filas/columnas? Realmente necesito hacer merge/span (unión) de columnas o filas? 
- Utiliza un caption o título a la tabla <caption>
- Agrega los atributos de scope en cada fila, para ayudar al usuario lector de pantalla a identificar cada elemento de la tabla

<table class="table">  <caption>Actividades educativas por día</caption>
<tr>
<th scope="col">Horario</th>
<th scope="col">Lunes</th>
<th scope="col">Martes</th>
<th scope="col">Miércoles</th>
</tr>

<tr>
<th scope="row">09:00 - 10:00</th>
<td>Arte</td>
<td>Matemáticas</td>
<td>Geografía</td>
</tr>

<tr>
<th scope="row">11:00 - 12:00</th>
<td>Historia</td>
<td>Química</td>
<td>Física</td>
</tr>
</table>

```html
<table class="table">  <caption>Actividades educativas por día</caption>

<tr>
<th scope="col">Horario</th>
<th scope="col">Lunes</th>
<th scope="col">Martes</th>
<th scope="col">Miércoles</th>
</tr>

<tr>
<th scope="row">09:00 - 10:00</th>
<td>Arte</td>
<td>Matemáticas</td>
<td>Geografía</td>
</tr>

<tr>
<th scope="row">11:00 - 12:00</th>
<td>Historia</td>
<td>Química</td>
<td>Física</td>
</tr>

</table>
```