---
id: 20121201
title: "El peor/mejor escenario posible con JS y XSS que se me ocurre"
date: 2012-12-01T11:27:07+00:00
author: Gorka
layout: post
permalink: /2012/12/el-peor-mejor-escenario-posible-con-js-y-xss-que-se-me-ocurre/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2012/12/worm.gif" alt="Computer Worm" />

Sin entrar a muchos detalles (eso lo haré en otro post), tuve la idea de hacer un programa que me permitiera en tiempo real conectarme a la sesión de un usuario en un browser en una página que yo controlo.

Hay muchas buenas razones para hacer algo así, yo lo pensé porque se podría ofrecer un servicio a clientes en tiempo real, algo que estaría muy cotorro (algo como el shared screen de skype).

Pero luego se me ocurrieron escenarios del ‘dark side’: si yo controlo el javascript en tiempo real de un navegador entonces el navegador es mío (de hecho aunque no sea en tiempo real, eso es xss). Y al tener eso las posibilidades son infinitas. Después de pensar un rato, se me ocurrió que hasta podría alargarse el ataque a otros websites (hoy en día gracias a peticiones asíncronas podríamos solicitar contenidos de cualquier web sin perder el control sobre el usuario – obviamente aqui hay una limitante de same origin petition pero hay maneras de saltar eso (server proxy o si el website final es vulnerable a xss directamente se envía al usuario a una url controlada)).

Esto no es nuevo, de hecho ya hay herramientas que permiten esto (BeEF), lo que no me convence es que se usa un server como centro de control y por lo tanto se puede rastrear el ataque. Entonces me puse a pensar que en lugar de conexión server – client podríamos hacer un programa que se conectara client – client, es decir, que una vez que se ejecutara el programa en un client hubiera manera de transmitirlo directamente a otros clients sin pasar por un server. Esto ayudaría mucho al anonimato (el problema es que el programa se perdería si el usuario cierra el browser, pero bueno si controlamos bien el browser y sus interacciones web entonces podemos tener una sesión bastante larga – y con un juego en tiempo real hasta podría existir el programa en ejecución siempre en browsers sin pasar por un lugar de persistencia).

Esto no es nada fácil, me refiero a conectar browser (sesión) con otro browser sesión, pero gracias a que html5 tiene websockets y que flash tiene sockets no es imposible.

Seguiré investigando y avisando si algo encuentro.

Saludos,<br />
Gorka

Un poco de investigación que había hecho:

- http://h3xstream.github.com/rtmfp-api/ (este usa un server)
- http://www.flashrealtime.com/local-flash-peer-to-peer-communication-over-lan-without-cirrus/ (este parece que funciona en LAN)
