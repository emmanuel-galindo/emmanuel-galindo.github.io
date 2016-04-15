---
published: true
title: GitHub Pages, Jekyll y TinyPress
layout: post
---
###Esta es una continuacion de mi articulo anterior
###Ya tenés el blog, ahora te cuento como agregarle comentarios, hacerlo mas ancho, etc

####Agregar comentarios
1. Generar cuenta en Disqus
..* Lo unico que necesitas es asignar un short name y acordartelo
..* Te va a dejar generar un código HTML universal para copiar en el blog, únicamente actualizando el shortname que seleccionaste antes.
+. Copiá de mi repositorio [Comments.html][1], al tuyo, en el directorio "_includes"
+. Agregá lo siguienteal archivo "_layout/default.html", aproximadamente en la linea 41, abajo de `{{ content }}`:
`{% include comments.html %}`

####Hacer que el blog sea mas ancho
1. Agregar un archivo custom.css en el dir "_css"
2.Agregar este contenido (1 rem aprox 16px, 16x62=992px)

```css 
@charset "UTF-8";

.measure {
  max-width: 62rem;
}
```

[1]: https://raw.githubusercontent.com/emmanuel-galindo/emmanuel-galindo.github.io/master/_includes/comments.html