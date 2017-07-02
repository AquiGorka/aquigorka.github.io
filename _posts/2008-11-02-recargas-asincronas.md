---
id: 80
title: Recargas Asíncronas
date: 2008-11-02T11:27:07+00:00
author: Gorka
layout: post
permalink: /2008/11/recargas-asincronas/
categories:
  - Ideas
---
**¿Qué es?**

Básicamente sirven para poder obtener información para enseñarla en una página Web sin tener que recargar toda la página.  Dado que las páginas muchas veces tienen información que siempre es la misma (menús, banners, footers, headers, sidebars, etc) es más rápido sólo recargar el contenido en sí.

**¿Que diferencia hay?**

Multiprocesamiento. Lo cual permite que todo sea más rápido.

**Tecnologías**

HTML es un lenguaje orientado a eventos (click o no click), es completamente síncrono, no pueden existir dos eventos al mismo tiempo. Es decir, un solo proceso de forma secuencial.

Flash y AJAX son tecnologías que pueden usar eventos asíncronos. Pueden existir tantos eventos simultáneos como el PC pueda llevar a cabo y pueden ser de muchos tipos diferentes (interacción con todos los periféricos de la PC). Es decir “N” número de procesos en forma totalmente descontrolada (pero controlada por event Handlers).

Aunque AJAX surgió mucho después de Flash, pronto se volvió muy popular (eso dicen unos amigos que tengo, hahaha, que nerd) porque se basa en Javascript y este lenguaje no le pertenece a nadie. En cambio Actionscript es de Macromedia (hoy en día de Adobe).

Todo este post es para presentar un tipo de recargas asíncronas que no requiere de ninguna de esas dos tecnologías y funciona de la siguiente manera:

En un HTML se carga un IFRAME invisible (este va a ser el espacio donde se va a cargar continuamente la información), y los necesarios DIV’s (pueden ser otros tags, pero estos funcionan bien) como contenedores.
La idea es que los links cargan la información en el IFRAME, luego se le saca el innerHTML y se manda al DIV correspondiente. Si todo está bien planeado y bien organizado no hace falta tener wrappers extras como XML para transportar datos sino que directo en el IFRAME se puede cargar la info tal cual se vaya a desplegar y punto.
Recargas asíncronas sin necesidad de aprender Actionscript (LoadVars o XML) ni AJAX (HTTPRequest).

Saludos,<br />
Gorka
