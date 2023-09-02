---
id: 20230831
title: "Snippets: WET y DRY"
date: 2023-08-31T00:00:00+00:00
author: Gorka
layout: post
permalink: /2023/08/snippets-wet-y-dry
categories:
  - Software Engineering
  - Technical Leadership
---

<img style="margin: auto;" src="/public/img/2023/08/snippets-wet-y-dry.png" alt="Wet vs Dry" />

> When you find yourself adding if statements to a piece of code in order to get it to behave differently under different scenarios, you’re creating a confusion. Don’t try to make one thing act like two things. Instead, separate it into two things.

No sé si estoy de acuerdo con este blog post: [Why I don’t buy "duplication is cheaper than the wrong abstraction"](https://www.codewithjason.com/duplication-cheaper-wrong-abstraction/). Tiene una opinión interesante y racional acerca de la situación código repetido vs la abstracción incorrecta, pero la frase me gustó mucho, creo que está bueno diferenciar "la abstracción incorrecta" de una "confusión" y creo que de ahora en adelante voy a usar el término.

Y definitivamente, voy a usar la frase de evitar hacer que una cosa funcione como dos cosas, en lugar implementa las dos cosas por separado.


Saludos,<br />
Gorka
