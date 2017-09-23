---
id: 20170923
title: No usar iris en Go
date: 2017-09-23T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/09/no-usar-iris-en-go/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2017/09/no-iris.jpg" alt="No iris" />

Me parece raro tener que escribir un post como este pero la verdad es que todo el contexto alrededor de este framewrok está muy raro/sketchy.

Cuento un poco de lo que he visto y luego lo que me pasó:

Desde este post en Hacker News [Iris framework author exposed for license violations](https://news.ycombinator.com/item?id=11976798) hablan de varias situaciones con el autor y como en repetidas ocasiones decidió editar/modificar/eliminar comentarios en contra suya. Este otro post [Why you should not use iris for your go](http://www.florinpatan.ro/2016/10/why-you-should-not-use-iris-for-your-go.html) hablá de esas situaciones y expone evidencia.

En su momento estuve haciendo un poco de research de frameworks para Go y al toque ecnontré iris y lo empecé a usar, hubo un par de releases (yo empecé por la 5 y llegó hasta la 7). Todo iba bien, y me gustaba lo que se podía hacer con esta herramienta.

De repente un día pasó algo raro: en el repo de github de iris (pueden verlo en este [fork](https://github.com/AquiGorka/iris) que hice) decía que habían comprado la herramienta y que ya no era de uso libre (o en realidad que le habían cambiado la licencia o que se yo) - por una startup de Dubai.

Y bueno, supongo que esto puede pasar, así que hice el fork para ver si por lo menos me quedaba con lo último que había actualizado, y ahí me di cuenta que habían sacado de la historia la versión 7 - supuse que esa era la que había vendido, en fin. hice mi downgrade para que todo siguiera funcionando.

Luego me avisaron (había un chat para los que usabamos el framework) que había otro fork que si tenía los últimos cambios: [Go-Speedo](https://github.com/go-speedo/go-speedo)y bueno, ahora empecé a usar ese, pero al toque este lo deprecaron y cambió a [Siris](https://github.com/go-siris/siris) y ahí me aburrí y decidí sacar el framework [aqui](https://github.com/AquiGorka/kickoff/commit/cb44d1f4a74a220e170e3a9d60b86d6f436b023e) - lo cual me hizo muy feliz ya que me dí cuenta que no lo necesitaba y que en realidad era demasiado para lo que yo estaba haciendo.

Eso fue hace unos meses, hoy de repente veo que el autor original tiene de vuelta el [framework](https://github.com/kataras/iris) y, que ya salió la [versión 8](https://github.com/kataras/iris/releases/tag/v8.4.2).

Así que no tengo ni idea que pasó, que pasa y como va a seguir y que va a seguir pasando, así que mi recomendación (al punto que estoy haciendo un post acerca del tema) es:

**No usar iris**

Saludos,<br />
Gorka
