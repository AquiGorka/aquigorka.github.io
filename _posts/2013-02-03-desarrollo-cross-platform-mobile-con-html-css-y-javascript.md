---
id: 20130203
title: Desarrollo Cross Platform Mobile con HTML, CSS y Javascript
date: 2013-02-03T11:27:07+00:00
author: Gorka
layout: post
permalink: /2013/02/desarrollo-cross-platform-mobile-con-html-css-y-javascript/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2013/02/Phonegap-Training.png" alt="Build Diagram" />

Siguiendo la línea de desarrollo mobile he estado desarrollando en un nuevo framework: en lugar de usar Actionscript3 de flash usé un StageWebView y el desarrollo fue directo en HTML, CSS y Javascript (con la ventaja que Safari Mobile – el engine del webview – puede entender la mayoría de tags de HTML5 y CSS3 – incluyendo transitions y transform).

Encontré un servicio (de un producto que ya tenía en mente exactamente para desarrollo con html) que lo que hace es tú le das tus archivos y ellos te compilan (vía cloud) para 7 u 8 plataformas diferentes (realmente a mí sólo me interesa iOS por ahora): PhoneGap Build (build.phonegap.com).

Lo que está muy cotorro es que para que funcione tienes que unir tu cuenta con un repositorio de github (para cada app) (gratis para repositorios abiertos y con costo para privados). Es una manera muy interesante que me forzó a meterme a ver más de Git y Github.

El API de phonegap está basado en el mismo API que se tiene con FLASH sólo que aqui le pegas desde Javascript (ya estuve viendo la documentación y la única real diferencia que vi es que no puedes hacer un embed en tiempo real de la cámara – y eso se usa bastante en realidad aumentada). Bastante completo y con posibles mejoras a corto y largo plazo que lo hacen una herramienta interesante.

Échenle un ojo y me avisan que les parece.

Saludos,<br />
Gorka

