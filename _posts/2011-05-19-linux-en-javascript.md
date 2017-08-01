---
id: 20110519
title: Linux en JavaScript
date: 2011-05-19T11:27:07+00:00
author: Gorka
layout: post
permalink: /2011/05/linux-en-javascript/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2011/05/zsh.jpg" alt="Zsh" />

Esto es muy divertido (y se une a algo que he estado pensando los últimos meses – pero aún no voy a mencionar, pero para que sepan que hay un pastelote en el horno..): un desarrollador encontró que hoy en día javascript (el no tan “poderoso” lenguaje que corre sobre el browser) es capaz de compilar y ejecutar Linux (un sistema operativo!).

http://www.readwriteweb.com/hack/2011/05/run-linux-on-javascript.php

La idea que javascript es un lenguaje limitado tiene que quedar atrás – y esto lleva implicaciones gigantescas en el área de seguridad informática – ya que claramente es capaz de muchas cosas, y aunque el ejemplo sea simplemente ejecutar un kernel de control sin GUI (no se puede ver, sino sólo tiene intérprete de comandos) debe ser suficiente para que los más “téchies” que critican el lenguaje se den cuenta de su “potencial”.

Cada vez más y más el navegador tiene más poder y control sobre nuestro uso de Internet y por lo mismo el lenguaje que se ejecuta en la computadora personal para “ayudar” o “mejorar” tal experiencia cada vez tiene más acceso al sistema en sí. El problema viene cuando una página web (la que sea) tiene control TOTAL sobre el javascript que se va a ejecutar:

**Basicamente el que programa la web tiene control total sobre el javascript del usuario (y lo mismo va para todas aquellas vulnerabilidades que rimen con XSS).**

Es decir, que cada vez es más y más peligroso simplemente hacer click (bueno, si consideran el ataque estilo “clickjacking” – como el que se ha visto en facebook últimamente – entonces ya ni siquiera eso..) y cada vez será peor.

¿Qué se puede hacer al respecto? No mucho realmente porque si sólo se considera la seguridad entonces hay que obviar la experiencia que puede brindar javascript (para los que no lo saben pueden usar NoScript de Firefox para eliminar javascript) pero eso está super chafa porque gracias a javascript tenemos grandes oportunidades como WebGL (páginas que pronto van a usar mnodelos y ambientes 3D sin límite), entonces? Pues yo la veo difícil, tal vez se implemente un header de javascript seguro o un “signed javascript” pero eso sigue dando permiso al desarrollador legítimo de usar nuestro browser como shell remoto de javascript… en fin, ya les iré avisando que pasa.

Saludos,<br />
Gorka
