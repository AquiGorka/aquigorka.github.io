---
id: 20171225
title: Emoji Trade
date: 2017-12-25T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/12/emoji-trade/
categories:
  - Ideas
---

<h1 style="font-size: 2em">
🐮 🤝 💸
</h1>

> Alemán: **kuhhandel** = **horse trading**<br />
> Holandés: **koehandel** = **cow trading**

Hace unos años me enseñaron este juego y desde ahí me gustó mucho. Al punto que cuando ibamos a acampar o había ganas de jugar algún juego de mesa decidía dibujar a mano los elementos necesarios para jugar.

Luego lo olvidé.

Hace poco se me ocurrió que estaría divertido hacer una versión en la que se usen los teléfonos celulares como control remoto para jugar este juego (la idea de los celulares no es nueva, ya lo hice con Tetris aquí: [Multiplayer Tetris](https://github.com/AquiGorka/multiplayer-tetris)).

Fueron un par de semanas divertidas, lo primero decidí hacer una versión para `npm` - que además resultó ser mi primer paquete publico de `npm`: [Kuhhandel](https://www.`npm`js.com/package/kuhhandel).

Paréntesis.

Para este desarrollo decidí usar [`lerna`](https://github.com/lerna/lerna) que es una herramienta para tener varios paquetes en un solo proyecto. Es más fácil para un proyecto así tener todo en un solo repositorio.

El tema es que para _continuous delivery_ tienes deploy de todo, y a veces no se hicieron cambios en todos los paquetes - por suerte los buckets que reciben los mismos archivos no cambian nada, así que en realidad es solo un poco de uso absurdo de recursos sin deploy real.

Lerna vale la pena.

Fin paréntesis.

El paquete para `npm` tiene (como es debido) tests y build. Y es parte de una idea que tengo de hace rato de hacer la parte de lógica de juegos como paquetes para descarga, y que luego cada quien les pueda hacer la interfaz visual como quieran.

Funciona sin servidores de `signaling` (pero con servidores de `shortening`) para hacer las conexiones `WebRTC` entre los clientes y se juega contra una _primera pantalla_ (que puede ser un iPad, una compu o una tele).

Para futuro agregaré otras funcionalidades:

- que se pueda ver el juego en otra pantalla (así se puede jugar a distancia)
- que se pueda jugar sin la primera pantalla (todos desde los celulares)

Así que bueno, eso, ahhhhh, y el catch divertido: el juego original usa animales de granja, yo decidí cambiarlo y que use `emojis`

[Emoji Trade](https://emoji-trade.got-game.net/)
[Kuhhandel @ github](https://github.com/AquiGorka/kuhhandel)

Saludos,<br />
Gorka

