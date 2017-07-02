---
id: 70
title: "Experimento #3: Sistema Experto de Información Global"
date: 2007-11-29T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/11/experimento-3-sistema-experto-de-informacion-global/
categories:
  - Ideas
---
Se propone un Sistema Experto que utilice toda la información publicada en Internet como base de conocimiento.

**Paso 1**: El sistema recibe una pregunta. El sistema analiza semánticamente la pregunta y reconoce la parte más importante para la búsqueda.
Ejemplo: ¿Qué es un átomo? Palabra clave: átomo

**Paso 2**: El sistema busca todos los documentos que contengan información relacionada a la pregunta. Es necesario que el sistema recopile todos aquellos documentos que estén relacionados a los primeros documentos y así sucesivamente con los nuevos documentos hasta que obtenga suficiente información acerca del tema.
Ejemplo: Todos aquellas documentos en Internet que contengan la palabra “átomo” y después buscará documentos que contengan cada una de las palabras de los textos con la palabra original y así sucesivamente hasta tener suficiente información.

**Paso 3**: El sistema analiza la información y genera una red de conocimiento acerca del tema. Una vez generada la red de conocimiento el sistema compara todos los documentos obtenidos para descartar aquellos que no cumplan con un nivel adecuado de semejanza a la red de conocimiento.
Ejemplo: Se genera una red de conocimiento con todas aquellas palabras, frases, enunciados y conceptos relacionados a lo que es un átomo. Se comparan los documentos con la red de conocimiento generada y aquellos que no tengan información semejante a la red se descartan.

**Paso 4**: El sistema crea un árbol lógico de conceptos para generar un resumen utilizando los documentos obtenidos. Hace esto subdividiendo conceptos hasta llegar a un concepto indivisible.
Ejemplo: Se explican las subpartículas que componen un átomo y luego se explican las subpartículas que componen las subpartículas del átomo hasta aquellas que no se puedan subdividir.

El sistema utilizará los algoritmos usados por los motores de búsqueda actuales, los cuales ya filtran una primera capa de información no pertinente a la búsqueda (esto para disminuir el tiempo de análisis con la red de conocimiento). El sistema puede utilizar datos estadísticos para generar respuestas a preguntas que no generen resultados directos, de tal manera que se le puede preguntar lo que uno quiera:

- ¿Qué resultado se obtendrá en algún evento deportivo?
- ¿Existe el Infierno?
- ¿Qué es Dios?
- ¿Puedo convertir a mi hermano en una lechuga?
- ¿Cuántas veces al año se recomienda tener sexo en lugares públicos?
- ¿Qué le pasa a Michael Jackson?
- ¿Existió de verdad el “chupacabras”?
- ¿Dónde está congelado Walt Disney?
- ¿Quién mató a JFK?
- ¿Dónde está Elvis?

El que pregunta decide el límite.

Saludos,<br />
Gorka
