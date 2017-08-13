---
id: 20111002
title: AS3 getdefinitionbyname y el compilador
date: 2011-10-02T11:27:07+00:00
author: Gorka
layout: post
permalink: /2011/10/as3-getdefinitionbyname-y-el-compilador/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2011/10/loophole.jpg" alt="Loopholes breakfast of lawyers" />

Sin abusar mucho (y no entrar a detalles MUY técnicos de OOP) estoy utilizando una clase de la librería de Flash AS3 que me permite instanciar clases de manera dinámica. Es una manera muy cómoda de eficientar procesos repetitivos (y de continuar con las ventajas de OOP como el polimorfismo) que nunca pensé que llegaría a utilizar (porque acostumbro declarar directamente las clases que voy a usar como propiedades privadas pero quise ver si podía quitar mucho código que se repetía sin sentido y encontré esta manera:

```AS3
var referencia_clase:Class = getDefinitionByName(string_clase) as Class;
instancia = new referencia_clase();
```

// si se preguntan por qué la instancia no tiene declaración formal es porque antes está declarada como un objeto “dinámico/genérico” que vía polimorfismo puedo reusar para distintas clases

Necesita un string con el nombre de la clase con lo que se hace una referencia a la misma y luego esa misma referencia se usa para instanciar el objeto de la clase en sí.

Con eso ya se tiene acceso (vía el objeto) a todos los métodos y propiedades.

PERO…

Por la manera en la que trabaja el compilador de Flash (en mi caso versión cs5.5) cuando se usa un “import” para traer clases a memoria para luego instanciarlas, el compilador sólo agrega a memoria las clases que sí tienen una llamada real (no hace falta instancia, puede ser nada más la referencia: var obj_clase:Nombre_Clase;).
Eso quiere decir que las clases que uno querría llamar de manera dinámica NO ESTÁN en memoria y por lo tanto cuando se ejecuta el código se tira un error de ejecución de variable nula.
Es un bug? No creo, es más como un loophole curioso ya que si con el import sí se trajeran a memoria las clases que se piden entonces el compilador perdería una super ventaja que tiene de eficientar las llamadas reales que tiene que hacer.

Entonces cómo se resuelve esto? Como lo puse arriba: haciendo una referencia como propiedad dentro de la clase que va a usar el getDefinitionByName => var referencia:Clase_Dinamica;

Aunque esto implica que se tienen que agregar todas las clases que se van a usar de manera dinámica una por una, aún así se puede aprovechar la función getDefinitionByName para eficientar códigos (igual habría que hacer realmente un benchmark de uso de recursos de instancias reales vs. referencia clases e instanciación de una en una para ver qué camino es mejor).

Espero esto ayude a aquellos que querían usar el método y les mandaba el error:

```AS3
ReferenceError: Error #1065: Variable nombre_de_la_clase is not defined
```

Saludos,<br />
Gorka

