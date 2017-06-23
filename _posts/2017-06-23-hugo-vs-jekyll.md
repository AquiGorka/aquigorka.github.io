---
id: 184
title: Hugo vs. Jekyll
date: 2017-05-28T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/06/hugo-vs-jekyll/
categories:
  - Ideas
---
<img src="/wp-content/uploads/2017/06/static.jpg" alt="Static site generators" />

> <p style="text-align: right; font-style: italic;">Managing software becomes central to the success of any businesses</p>

Y que mejor que probar las diferentes herramientas posibles. En este caso me puse a jugar con dos herramientas para blogs/websites estáticos (Hugo y Jekyll),

¿Qué son los generadores de websites estáticos?

Un poco de contexto: las páginas web son basicamente html (y js y css pero para hacerlo fácil, no digamos nada de eso). Y los navegadores saben que el contenido que viene en html se enseña de diferentes maneras (tablas, parrafos, links, menus, etc.). Entonces si uno agarra un editor de texto y escribe html y guarda el archivo y lo abre con google chrome entonces se ve una página web - así lo más sencillo de lo sencillo. Genial y estático, es decir que para cambiar el contenido de esa página habría que abrir el archivo y modificarlo y luego guardarlo de vuelta y abrirlo con chrome.

Pero y cómo hago (o como se hacía antes de los spas y ajax) para que las páginas tuvieran contenidos dinámicos - momento cerebrito, contenido dinámico?

¿Qué son los contenidos dinamicos?

Si entras a una página web que tenga sistema de registro y te loggeas y en algún lugar en la página te dan la bienvenida por tu nombre (ej "Bienvenido Gorka") bueno, ese nombre va a ser diferente para cada persona (que no tenga el mismo nombre no?), es decir, de manera dinámica se cambia el nombre de la persona que hace login.

Retomando, entonces para hacer eso, se usan lenguajes que funcionan en los servidores (de todos los sabores y colores que uno se pueda imaginar, y aqui es donde pueden llegar a sonar nombres como PHP, Node, Python, Java, Go, Ruby, Perl, etc.) que hacen eso mismo, cambian los contenidos de las páginas cada vez, y eso es, en sí, escribir el archivo html y mandarlo al navegador. Y pues aqui es donde se inicieron muchos sitemas de gestión de contenidos dinámicos (otros nombres como Wordpress, Joomla, Drupal, etc.).

Pero ese dinamismo viene con un costo, es decir, el tiempo que el servidor se toma para saber qué contenidos escribir (y hasta de dónde sacar los contenidos en sí). Así que para evitar caer en esos "costos" algunas personas decidieron desarrollar programas de gestión de contenidos que generan páginas estáticas. Esto viene con otros costos, pero como este blog post es super introductorio, eso lo explicaré en otra ocasión.

En fin, así que probando los sistemas, dejo mi opinión: prefiero Hugo - con todo y que este mismo blog usa Jekyll.

Voy a seguir usando ambos, y eventualmente haré posts de como instalar y usar cada uno.

Las ventajas de ambos: mis dos blogs (este y AquiGorka.net) van mucho más rápidos, y al estar ambos hosteados como contenidos estáticos también es mucho más barato.

Se me hizo medio largo el post de introducción, así que acá lo dejo por ahora.

Saludos,
Gorka
