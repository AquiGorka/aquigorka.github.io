---
id: 232
title: Seguridad en desarrollos en Internet
date: 2011-01-17T11:27:07+00:00
author: Gorka
layout: post
permalink: /2011/01/seguridad-en-desarrollos-en-internet/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2011/01/seguridad.jpg" alt="Seguridad" />

¿Qué ondas con esto? El enfoque que le voy a dar es el siguiente:

Un cliente me pide que analice su página web y su tienda virtual. Al hacerlo me doy cuenta que usaron un sistema abierto y conocido para la tienda (joomla con virtuemart) y que la página está muy mal hecha (no tanto de diseño sino de sistema/funcionalidad).

Al revisar un poco la parte de la tienda me doy cuenta que el sistema que usan tiene errores de seguridad (y para esto ni siquiera me puse a buscar errores por mi parte, sino simplemente busqué en google por vulnerabilidades del mismo).

Le hice saber a mi cliente que hay problemas por ese lado, a lo cual me preguntó **“qué es lo peor que puede pasar? – me quitan la web y luego?”** y yo le respondí con un caso hipotético (pero real) con lo que se dió cuenta de la importancia del problema.

El problema no tiene tanto que ver con lo que le dije que puede pasar, sino que en Internet se tiene campo abierto para desarrollar/hacer/imaginar escenarios de ataques, entonces cualquier otro podría imaginar su propio tipo de ataque y llevarlo a cabo.

Entonces ahora queda lo siguiente: le tengo que hacer llegar a mi cliente un presupuesto con el cual revisaremos el sistema y buscaremos proteger/filtrar la información para que no lo puedan atacar. A esto mi cliente me va a preguntar **“es 100% necesario que yo haga esto?”** y ahí es donde viene mi reflexión:

Vivimos en un mundo en el que realmente si alguien quiere atacarte hay miles de maneras de hacerlo (y esto no solo pensando en el mundo digital), en serio, si alguien tiene algún rencor directo contra tí puede hacer tantas maldades/ataques sin que lo puedas atrapar que en general decidimos no volvernos la cabeza loca con toda la histeria que eso podría generar (cuántos de ustedes llevan a cabo verdaderas prácticas de 100% seguridad? – un amigo deja su departamento sin llave; otro nunca cierra su coche; otros usan facebook y foursquare; la mayoría de mis amigos argentinos toman mate usando la misma bombilla – es riesgo de seguridad en cuanto a higiene/salud – in a word herpes; cuántos se fijan si alguien los está vigilando al entrar a un banco? en fin… ahí deben encontrar un ejemplo que les caiga).

<p style="text-align: center;">¿Debería ser igual para Internet?</p>

<p style="text-align: center;">¿Deberíamos decidir no volvernos locos por todo lo que podría pasar, sabiendo que si realmente alguien nos va a atacar es 100% seguro que encuentre una manera de hacerlo?</p>

Es decir, además de lo que hacemos diario, ahora también tenemos que preocuparnos por buenas prácticas de desarrollo en cuanto a seguridad en nuestros negocios en Internet?

**SÍ**

Y lo más molesto, es que SÍ te tienes que poner a entender como son los ataques en Internet. No tanto a nivel técnico, pero si a nivel sustancia, de la misma manera que entiendes como en Ocean’s 11 logran encontrarle los “ángulos” a los procesos para lograr atacar, es necesario que el usuario promedio entienda la manera en que se pueden llevar a cabo ataques en web y eso por una palabra: **escalabilidad**.

Un sólo error en seguridad en un sistema, compromete a todos los sistemas que están montados sobre este (esto es de Matrix Reloadad, hahaha) así que es importante llevar a cabo buenos desarrollos en cuanto a seguridad de la misma manera que se hacen buenos desarrollos en cuanto a funcionalidad – el problema, es que a la hora de la lana, los clientes deciden dejar de lado esas prácticas para “después” (y ni siquiera caigo en el típico “lo barato sale caro” porque puede ser que nunca te ataquen) pero es como dejar la puerta abierta, es un acto de fé creer que no te va a tocar a tí (y claro, cuando te toca siempre viene el “¿por qué a mí? hahahaha).

Así que bueno, yo trataré de hacer mi papel y recomendar las buenas prácticas, el universo dirá si los planetas se alinearon y ahora los empresarios ya toman en serio las cuestiones de seguridad en Internet como primordiales.

Saludos,<br />
Gorka

P.D. – para todos los que dicen, “a mí no me toca”, “eso que, yo ni tengo negocios en Internet”, nada más busquen lo que es “Fire Sheep” a ver si no les hacen un robo de identidad en Facebook (y otros..)  por andar de confianzudos...
