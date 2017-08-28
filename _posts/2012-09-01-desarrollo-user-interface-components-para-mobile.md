---
id: 20120901
title: Desarrollo User Interface Components para mobile
date: 2012-09-01T11:27:07+00:00
author: Gorka
layout: post
permalink: /2011/09/desarrollo-user-interface-components-para-mobile/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2012/09/ux-discussion.jpg" alt="UX Discussion" />

Como parte del desarollo de apps en el que he estado participando (mobile para iOS y Android), tuve que decidir crear/recrear elementos típicos de interacción con el usuario (UI / UX elements).

Aquí la lista de los que ya he desarrollado:

- Botón
- Lista Vertical (witdth y height definibles y con inertia para darle el touch & feel nativo)
- Lista Horizontal (hereda funcionalidad de lista vertical)
- Lista en Grid
- Image Holder
- Image Swiper (en forma de matriz)
- ComboBox
- Scroller (para textos, fotos, ambos, etc)
- FileChooser
- PicTaker (este hace todo sin mandar a la funcionalidad de camara nativa – pro’s y contra’s)
- Símbolos (uso de una librería gráfica vectorizada)

De las cosas mas divertidas ha sido que he aprendido mucho a usar herencia y polimorfismo para reusar código y así hacer las cosas mas fáciles pero de mayor complejidad. Con esto logre crear los siguientes:

- Listas donde se pueden eliminar elementos
- Listas que se pueden manipular el orden de los elementos
- Listas de despliegue secuencial (favorecen mucho el desempeño)
- Listas que mezclan ambos delete y edit
- Listas dentro de Listas (horizontales dentro de verticales pero viceversa es posible)

Lo que me gustó mucho, es que aprendí a hacer estos componentes de una manera que se pueden heredar y sobreescribir, esto es MUY chido porque así puedo cambiar cosas específicas de manera de desplegar (no tanto de funcionalidad ya que esa se deja igual) y así puedo pintar/dibujar los diferentes elementos de los componentes como cada proyecto lo necesite – sin tener que configurar directamente en cada elemento.

Mi idea es hacer un libro app para iPad donde pueda explicar todos estos elementos (y más, desde como preparar un ambiente de desarrollo y cómo publicar) y el caso de uso de la app sería el mismo libro (es decir, en cada sección del libro usar los mismos elementos a manera de tutorial).

Probablemente buscaré meter el proyecto en idea.me para ver si así logro pagar el desarrollo, ya les pediré ayuda entonces.

Saludos,<br />
Gorka

