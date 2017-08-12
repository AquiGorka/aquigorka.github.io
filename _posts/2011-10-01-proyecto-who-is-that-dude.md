---
id: 20111001
title: "Proyecto: Who is that dude?"
date: 2011-10-01T11:27:07+00:00
author: Gorka
layout: post
permalink: /2011/10/proyecto-who-is-that-dude/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2011/10/facial-recognition.jpg" alt="Facial Recognition" />

La idea: estás viendo una pelicula o una serie de televisión (es más hasta una revista), no sabes como se llama el actor/actriz que está frente a tí, así que sacas tu iphone abres tu app de Who’s that dude? enfocas su cara y puf! magicamente te saca los datos del actor de IMDB. En la pantalla del iphone saldría un cuadro donde tienes que poner la cara del actor (y esto puede ser difícil si las cosas se están moviendo pero eventualmente podemos hacer que sólo con que se vea la cara en la pantalla se le reconozca.

La idea es que la app manda fotos de la cara a un servidor, este servidor se encarga de hacer el reconocimiento (con una base de datos de caras y celebridades preparada desde antes) y cuando encuentra un match manda pedir los datos a algún servicio de IMDB (hay que revisar que exista esto o sino usar su feed de XML o sino hasta parsear sus HTML’s) y eso se enseña al usuario en el iphone.

**¿Qué necesito para hacer esto?**

- funcionalidad de web (es decir si para que esto funcione sea WIFI o 3G el dispositivo tiene que estar conectado a Internet)
- programa que se encargue del reconocimiento facial y que tenga una base de datos (esto no es taan fácil y la base de datos puede ser MUY grande así que hay que calcular y organizar bien esta parte)
- programa o script que se conecta a IMDB una vez que se sabe que actor/actriz es y que obtiene los datos del mismo
- funcionalidad básica de app (secciones, botonería, eventos, etc)

Tengo ya varias ideas de cómo hacer la parte del servidor del reconocimiento facial, pero hasta que haga pruebas prefiero no contar demasiado.

Eventualmente si sale este proyecto, voy a hacer uno similar que use los datos y fotos de Facebook y que funcione para cualquier persona pública.

Saludos,<br />
Gorka

