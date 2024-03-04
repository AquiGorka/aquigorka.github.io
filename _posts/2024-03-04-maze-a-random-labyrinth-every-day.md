---
id: 20240304
title: "Maze: a random labyrinth every day"
date: 2024-03-04T00:00:00+00:00
author: Gorka
layout: post
permalink: /2024/04/maze-a-random-labyrinth-every-day
categories:
  - Games
  - Random
  - Social challenge
---

<img style="margin: auto; height: 500px;" src="/public/img/2024/03/maze.png" alt="A new labyrinth every day" />

Hace mucho tiempo que tengo ganas de jugar con [r3f](https://docs.pmnd.rs/react-three-fiber/getting-started/introduction), es una librería (o colección de librerías) para crear ambientes virtuales 2D y/o 3D en el browser con React. También hace mucho que quiero hacer más software de entretenimiento (aka video juegos). Ahora que tengo un poco de tiempo en mis manos, decidí empezar a ver qué podría hacer.

Empecé por ver si podía simular un ambiente 3D con colisiones y una vista aerea que _casi, casi_ hiciera ver el ambiente como 2D. Una vez que logré esto, quise ver si podía "escuchar" eventos del ambiente virtual y enseñar modales con HTML - esto es para lograr de manera efectiva unir el componente canvas que dibuja el ambiente, con controles en HTML y así "unir los dos mundos". Lo logré de manera exitosa.

Tenía muchas ideas, muchas ganas de hacer cosas muy grandes, pero para empezar bien decidí hacer algo "corto, y al pie": un laberinto.

Para esto tuve que buscar la manera de 1) definir una salida y definir un camino hacía la salida, 2) al azar posicionar paredes para hacer efectivamente un laberinto pero que las paredes no cerraran el camino hacía la salida. Una vez que logré estos dos, se me ocurrió "tapar" la vista, de tal manera que solo al moverse por el laberinto se puede "ver" las paredes y el camino recorrido.

Ya con esto, le sume una dinámica social al estilo [wordle](https://www.nytimes.com/games/wordle/index.html), donde se hace un "dibujo" de la solución, con el número de pasos que se tomaron para encontrar la salida. Esto para ayudar a hacer un tipo de competencia por ser quien llega a la salida en el menor número de pasos.

De aquí salió [Maze](https://maze.aquigorka.com/), un juego que crea un laberinto diferente todos los días, donde al encontrar la salida puedes compartir tu solución en X.

Saludos,<br />
Gorka
