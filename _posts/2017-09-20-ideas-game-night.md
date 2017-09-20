---
id: 20170920
title: "Ideas: Game Night"
date: 2017-09-20T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/09/ideas-game-night/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2017/09/game-night" alt="Game Night" />

Entre todas las ideas que estoy desarrollando se me ocurrió que podía usar el smartphone para controlar juegos (esta es la idea original, viene desde hace años - desde poco después que terminé el viaje de TrotaMexico) y poco a poco fui encontrando como hacer esto.

Pasé por varios experimentos, el primero fue una app que ejecutaba un server en la compu y via socket.io comunicaba el smartphone con el contenido visual (https://github.com/AquiGorka/remote-device). Esto lo hice con algo que se llamaba `node-webkit` (la primera versión de lo que hoy se llama `electron`) y luego me encontré con `webRTC` y de ahí salieron varios experimentos:

- el celular sincronizado (si tenías un android podías transformarlo en iPhone): http://remote-device-theater.surge.sh/#/
- el `sarcasm-o-meter` o _sarcasmometro_: http://sarcasm-o-meter-server.surge.sh/#/
- `Puppets` (uno de mis favoritos): https://github.com/AquiGorka/puppets
- Un PoC (prueba concepto) para usar el smartphone como linterna en una escena oscura de realidad virtual: https://github.com/AquiGorka/adventures-with-webvr

Y después quise seguir con la idea original, así que busqué un juego de `Tetris` open-source que pudiera utilizar y lo uní con el celular para controlarlo y luego puse dos juegos de estos a competir al mismo tiempo en formato supervivencia: https://github.com/AquiGorka/multiplayer-tetris

Pero ahí no quedó la cosa. Hoy estoy trabajando en una capa encima donde las personas pueden participar de manera grupal, es decir, haciendo un "torneo" o una "noche de juegos" y que cada persona pueda unirse con su celular y jugar cuando sea su turno.

La idea es tener un "leaderboard" para ir viendo quien va ganando más en la noche y luego ir agregando más juegos.

Esto es una idea en desarrollo aún, ya iré contando más cuando la vaya probando.

Saludos,<br />
Gorka
