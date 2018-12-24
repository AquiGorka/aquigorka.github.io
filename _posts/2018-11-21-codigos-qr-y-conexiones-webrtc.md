---
id: 20181121
title: "Códigos QR y conexiones WebRTC"
date: 2018-11-21T21:03:07+00:00
author: Gorka
layout: post
permalink: /2018/11/codigos-qr-y-conexiones-webrtc/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2018/11/webrtc-qr.png" alt="WebRTC QR" />

El mes pasado publiqué uno más de mis experimentos. Era un viernes cualquiera y como otras veces decidí compartir en varios lugares el link para ver si conseguía algún tipo de feedback. Cual fue mi sorpresa cuando el post consiguió tracción en [`Hacker News`](https://news.ycombinator.com/) y se quedó todo el día en la front page y luego fue trending en GitHub/JavaScript. Tremenda nerd-felicidad.

Les doy un poco de contexto:

Para hacer una conexión WebRTC se necesita intercambiar información de cada uno de los devices (entre otras cosas imagino que datos de IPs y similares) y hay diferentes maneras de hacer este intercambio. Lo más "normal" es un usar un servidor que se llama servidor de `signalling`. El dispositivo `A` se conecta al servidor y le dice soy `A`, luego llega el dispositivo `B`, que se conecta y hace lo mismo (me llamo `B`). `B` le pregunta al servidor: "¿conoces a `A`?" y el servidor le dice si, y se encarga de pedirle a cada dispositivo la info correspondiente, la intercambia entre ellos y así al final `A` se conecta directamente a `B` (y puede intercambiar datos directamente sin usar el servidor). Así se establece una conexión en tiempo real (Web Real Time Communication).

Mi problema es usar un servidor de `signalling`. Tiene demasiado "poder" ya que al final es quien decide que dispositivos se conectan entre sí. Si fuera "malicioso" podría hacer un ataque en el cual conecta a `A` <-> `C` <-> `B`, sin que `A` o `B` lo sepan y sus comunicaciones podrían ser escuchadas y hasta alteradas.

Mi experimento busca establecer una conexión WebRTC sin usar un servidor de `signalling`. Para eso busqué la manera de intercambiar los datos de `signalling` usando códigos [`QR`](https://en.wikipedia.org/wiki/QR_code). La información es más de lo que se puede transmitir en un sólo código QR por lo que tuve que hacer una secuencia de códigos (uno tras otro), donde cada uno transmite la parte que le toca y más información (el total de slides y el índice de si mismo para que el dispositivo que está leyendo sepa como va y cuanto falta).

El experimento funciona y se puede, de manera completamente descentralizada establecer una conexión WebRTC en una red ad hoc.

Ya tengo pensado otro tipo de usos para esta tecnología que iré contando después, por ahora les dejo el link al post en HN: [`Show HN: WebRTC signalling data using QR codes`](https://news.ycombinator.com/item?id=18201958).

Saludos,<br />
Gorka
