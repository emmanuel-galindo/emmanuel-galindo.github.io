---
published: true
title: GitHub pages desde linea de comando
layout: post
---
###Los ejemplos son para Linux Debian, pero los pasos son los mismos###

1. Instalar git (como root): 
`# aptitude install git`
+ Ir a tu repositorio de la pagina en GitHub y copiar la url (aparece entre HTTPS y el botón Download ZIP)
+ Localmente, ir al directorio donde querés trabajar
+ Clonar el repositorio (como usuario normal) usando la url del paso 2)
`$ git clone https://github.com/emmanuel-galindo/emmanuel-galindo.github.io.git`
+ Modificar algun archivo como prueba
+ Ejecutar:
`$git commit -a -m "Commit"; git push origin master`
+ Va a solicitarte usuario y password. Para evitar cargarlo en cada push, se lo puede cachear con dos comandos`:
`$git config --global credential.helper cache`
`$git config --global credential.helper 'cache --timeout=3600'

3600 segundos, es una hora... durante esa hora, no va a  pedir las credenciales luego de la primera vez que se especifiquen.
