---
id: 20110504
title: "¿Cómo entrarle al desarrollo de apps para iPhone?"
date: 2011-05-04T11:27:07+00:00
author: Gorka
layout: post
permalink: /2011/05/como-entrarle-al-desarrollo-de-apps-para-iphone/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2011/05/apps.jpg" alt="Apps" />

La cosa es así: ¿qué se necesita para hacer apps para iOS? y que sea sencillo de entender.

**Primera versión** (la orginal, la tradicional, la apretada de apple porque de “a fuerzas” necesitas una Mac):

Para “desarrollar” o “programar” para iOS se necesita descargar una serie de “librerías” con las cuales la secuencia del programa queda lista para poder “funcionar” en todos los dispositivos o gadgets que usan iOS – ipod touch, iphone, ipad.

Esas librerías se descargan gratuitamente del sitio de desarrolladores de apple (developer.apple.com) con un sencillo y gratuito registro.

Hay que instalar esas librerías en tu Mac (sólo se pueden instalar en una Mac) y con eso ya tienes listo los programas para hacer apps (bueno, casi porque ahora necesitas programar en Objective C con estructura/arquitectura de Cocoa y Xcode).

Fácil no?

**Segunda versión** (la peleada, la terca, la que demostró que la “banda” puede más que el capricho de algunos):

Se puede usar Flash CS5 para desarrollar/programar apps. Hay que descargar una serie de librerías (también gratuitas del sitio de Adobe – luego agrego el link) y con eso al iniciar un nuevo proyecto se puede seleccionar la opción de apps.

Esta versión fue muy peleada porque por mucho tiempo no Apple no quería que ningún programa de fuera pudiera crear apps y hasta llegaron al punto en que dijeron que no iban a aceptar apps hechas de esta manera, pero le pegaron a Apple porque ellos siempre dijeron ser de mente abierta y desarrollo abierto para todos – pero crearon un esquema tan cerrado que demostraba ser contrarío a su filosofía – al final, se rindieron y hoy en día aceptan apps de esta manera.

El problema es que esas librearías tienen alcance limitado y no pueden todas las usar herramientas al alcance como la cámara, geolocalización, el giroscopio, entre otras. Y además no se puede agregar código que se ejecute en “run time” porque no hay un intérprete de actionscript (esto de hecho se me hace muy chafa pero por seguridad lo puedo entender) y sólo necesitas aprender AS3 y flash.

Más fácil pero muy chafa no?

**Tercera versión** (ya la de perdida, la que nos queda, la “no tan” cerrada):

Usar un SDK de un framework externo que si tenga acceso a las herramientas que flash no puede. Porque hay cuates que vieron el negocio de flash y lo quisieron mejorar con el slogan de “si tu puedes hacer una página web con HTML5, CSS3 y Javascript (y hasta algún lenguaje de script como php) entonces vas a poder hacer una app”.

Esto para invitar a TODO mundo a entrarle a este tipo de desarrollos, con el catch que para usar este tipo de  herramientas en su máximo potencial todavía se necesita comprar una Mac ya que al final del día la “compilación” tiene que ser hecha con el “toolchain” de Mac – y ni pregunten porque yo todavía estoy entendiendo esta parte.

Entre los frameworks que se pueden usar para esto están Titanium y DragonFire.

Chido pero aún caro no?

**Cuarta versión** (la hacker, la barata, la accesible para todos aquellos con conocimientos técnicos MUY elevados):

De los mismos creadores del jailbreak, de cydia y de muchas de las grandes maravillas que la gente pelea porque quieren recuperar la libertad de “hacer lo que se le de la gana con los gadgets que compra” – Saurik – encontró la manera de imitar ese “toolchain” de Mac con lo cual se pueden compilar apps para iOS desde otros lenguajes similares (como C, C++, Java y derivados de bajo nivel).

Esto para que todos aquellos interesados en crear apps desde Linux lo puedan hacer. Pero la verdad es que se necesitan conocimientos técnicos MUY avanzados, casi tanto que en lugar de aprender a hacer esto es más fácil y barato aprender código de Objective C y comprar una Mac (ese es mi caso).

Super chido pero NADA fácil..

**Quinta versión** (la socialista (hasta que pegue y empiecen a cobrar) y novedosa y de geeks muy inteligentes):

Unas personas proponen lo siguiente: haz, desarrolla, programa en lo que sea que se te de la gana (no tan así pero hay amplio espectro de lenguajes y arquitecturas aceptadas) y luego pásanos tus códigos fuente y nosotros compilamos y te regresamos tu app.

Sea windows, mac, linux o lo que sea, les envías los códigos fuente y ellos lo pasan por una Mac (o ve tu a saber si por el una manera estilo la cuarta versión) y después te regresan la app lista para vender en app store. Así no tienes que comprar una mac ni aprender un lenguaje nuevo – PERO – tienes que confiar en darle tus códigos fuente a alguien más y confiar en que no modificaron, copiaron, piratearon, voltearon, jugaron, vieron, editaron nada y te dieron algo a cambio (y hasta ahora gratis) – estoy hablando de phoneGap.

Super duper chido pero demasiado comprometido y falto de confiabilidad (si es que se entiende)..

Así que bueno, este es un primer análisis. Hay muchas maneras y cada vez llegarán más pero serán similares a esto que explico. Por ahora lo que puedo recomendar es tomar el camino de menos esfuerzo según el conocimiento técnico de cada uno: para los genios el #4, para los no tan genios el #1, para los que tienen el billete y no llegan al dos pues el #3, para los que no les importa tanto el alcance la #2 y para los confiados el #5.

Espero esto ayude a tomar el camino correcto. Yo sigo decidiendo por donde voy a ir y seguiré escribiendo de mi experiencia en general en este tipo de proyectos/emprendimiento.

Saludos,<br />
Gorka
