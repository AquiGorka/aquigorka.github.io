---
id: 20130601
title: Javascript Frameworks
date: 2013-06-01T11:27:07+00:00
author: Gorka
layout: post
permalink: /2013/06/javascript-frameworks/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2013/06/framework.jpg" alt="Framework" />

A fines del año pasado decidí que iba a ver como era el desarrollo de apps vía HTML5 (se usa un wrapper nativo que hace como si abriera una página web – todos los archivos están locales). Los resultados me gustaron mucho, al punto que decidí dejar por ahora el desarrollo en AS3 (ojo, hay cosas que no puedo hacer con javascript que seguro tendré que hacer con AS3 – estoy hablando de socket servers, pero bueno… para otro post).

En su momento me puse a analizar cómo iba a trabajar, mis opciones eran aprovechar el framework que ya tenía para AS3 (traerlo a javascript no sería nada difícil) o ver que opciones había. Encontré que hay muchas herramientas, estrucutras, código, ayuda para hacer este tipo de desarrollos (lo cual sería medio obvio ya que la mayoría de estas se usan en web). Entre los que más me llamaron la atención están EmberJS, AngularJS, Backbone y MeteorJS (los otros que encontré no tenían detalles o malas reseñas o comparaciones contra estos). De estos 4 me decidí aventurar por EmberJS – con una propuesta muy innovadora y una fuerte comunidad atrás del proyecto (ojo los otros también, pero en comparaciones este parecía salir ganando) y con una cosa que fue lo que me hizo voltear: ofrecía una estructura que une modelo con vista de manera automática (tiempo después me enteré que AngularJS también lo tiene pero en su momento no lo vi, en fin…).

Por unos meses jugué con EmberJS, traté de hacer funcionar las cosas, traté de hacer funcionar su estructura de DStore (EmberData) pero lamento decir que el framework no estaba en momento maduro y que, por lo mismo, tomé la decisión de hacer las cosas con mi propio framework. PERO – algo que me había gustado mucho era la manera de trabajar de EmberJS con un estilo MVC muy marcado, así que decidí incorporar eso a mi nuevo javascript framework – el cual tuve listo en menos de 2 semanas y con eso logré publicar una app (ya lo he contado: Mendoza Wineries).

Hace un par de semanas he estado jugando con otra herramienta que se llama KnockoutJS – sería la pieza clabe que le faltaba a mi framework: unir modelo-vista de manera automática. Debo decir que ahora que ya lo logré hacer funcionar y entiendo sus conceptos estoy FASCINADO, no sé como pude trabajar sin un modelo así antes – en su momento me quejé que lo que exige EmberJS es olvidar el modelo de manipular el DOM y ahora, me parece obvio y completamente congruente.

Creo que es un buen momento para darle otra oportunidad a EmberJS – ya están en versión 1 – y ver que sale. Dependiendo de ese experimento decidiré si seguir por ahí, hacer pruebas con algún otro (AngularJS le tengo muchas ganas también) o si mejorar mi propio framework con KnockoutJS directamente. Ya les iré avisando.

Saludos,<br />
Gorka

