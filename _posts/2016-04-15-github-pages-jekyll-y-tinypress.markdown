---
published: true
title: GitHub Pages, Jekyll y TinyPress
layout: post
---
### Esta es una continuacion de mi articulo anterior

### Ya tenés el blog, ahora te cuento como agregarle comentarios, hacerlo mas ancho, etc

#### Agregar comentarios
1. Generar cuenta en Disqus
..* Lo unico que necesitas es asignar un short name y acordartelo
..* Te va a dejar generar un código HTML universal para copiar en el blog, únicamente actualizando el shortname que seleccionaste antes.
+. Copiá de mi repositorio [Comments.html][1], al tuyo, en el directorio "_includes"
+. Agregá lo siguiente al archivo "_layout/default.html", aproximadamente en la linea 41, abajo de `{ content }` :
{% highlight text %}
{% raw %}
{% include comments.html %}
{% endraw %}
{% endhighlight %}

####Hacer que el blog sea mas ancho
1. Agregar un archivo custom.css en el dir "_css"
+ Agregar este contenido (1 rem aprox 16px, 16x62=992px)

```css 
@charset "UTF-8";

.measure {
  max-width: 62rem;
}
```

####Modificar el color de la caja para codigo fuente###
Para cambiar el color de fondo de los bloques de codigo, por ej en [Yarssr is not loading the feed, how to fix it][2]:
1. Abrir default.html en "_layout"
+ Modificar la línea:

{% highlight html %}
    <link rel="stylesheet" href="{{ "/css/solarized-dark.css" | prepend: site.baseurl }}" type="text/css">
{% endhighlight %}
por
{% highlight html %}
    <link rel="stylesheet" href="{{ "/css/solarized-light.css" | prepend: site.baseurl }}" type="text/css">
{% endhighlight %}

O viceversa...

####Eliminar la barra de desplazamiento (scrollback) horizontal de los bloques de código, y que muestre el codigo wrapeado
Yo se, la idea es que sea de facil lectura, pero yo acostumbro a no escribir lineas de mas de 80 columnas.


[1]: https://raw.githubusercontent.com/emmanuel-galindo/emmanuel-galindo.github.io/master/_includes/comments.html
[2]: http://emmanuel-galindo.github.io/2016/04/14/yarssr-is-not-loading-the-feed-how-to-fix-it.html]
