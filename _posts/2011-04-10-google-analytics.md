---
id: 20110410
title: Google Analytics
date: 2011-04-10T11:27:07+00:00
author: Gorka
layout: post
permalink: /2011/04/google-analytics/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2011/04/analytics.png" alt="Google Analytics" />

Por mucho uno de los mejores y más completos sistemas de estadísticas que se puede usar para cualquier web. Lo mejor que tiene es sin duda su flexibilidad/configurabilidad, aunque la facilidad de uso compite también.

Es poco probable ya en estas fechas que alguien no incluya los códigos javascript de este servicio en las páginas que desarrollan pero aún así quiero invitar a todos aquellos que no lo hacen a probar este sistema (el cual uso desde hace ya mucho tiempo y me parece increbile).

La idea es simple, se incluye un código en todas las páginas de las que se quiere llevar estadísticas (generalmente se puede incluir en los archivos de template para no tener que copiar de uno en uno en todos los archivos) y a manera sencilla les explico que lo que hace este script es solicitar de los servidores de google una imagen y de ahí vía información de los headers html, de todo lo que se puede obtener vía javascript (tiempos de interacción, información de la pantalla del usuario – no tanto de navegador porque eso viene con los headers, tiempo de visita) y de una cookie que deja (así lleva otros datos como visitas únicas, repetidas en cierto periodo de tiempo, visitantes recurrentes, etc.

En una interfaz increiblemente sencilla (que están por cambiar por lo que supone una más intuitiva y amigable) te dan los datos obvios necesarios (por un rango de tiempo seleccionado):

- visitas
- páginas vistas
- promedio de páginas vistas por visitante
- promedio de salida (bounce rate) – es un concepto muy interesante: qué tanto las personas entran y luego luego se van sin visitar otra página
- tiempo promedio de las visitas (contando todas las páginas visitadas)
- tiempo promedio de las visitas a cada página
- porcentaje de nuevas (y por lo tanto de recurrentes) visitas
- datos de continente, país, región, ciudad (y en usa hasta distrito) de dónde son las visitas
- procedencia de las visitas
- keywords que generaron entrada en las visitas que vienen de buscadores
- un detalle completo de todo esto a nivel total y página
- detalle de páginas de salida
- detalle de páginas de entrada
- detalle de flujo de las visitas (para entender dónde se pierde a los visitantes)
- etc., etc., etc.

Sin entrar a detalle de explicar esos términos lo que quiero es explicar porque me parece lo mejor la flexibilidad y configurabilidad de este sistema:

Flexible en el sentido que se pueden generar otro tipo de reportes que no tienen NADA que ver con lo anterior y tiene que ver con el tipo de interacción que se lleva a cabo con las páginas web – directamente tiene que ver con eventos. Digamos una web de descargas puede llevar estadísticas de cuantas veces se descarga un archivo pero eso no nos dice nada sin el contexto, bueno con GA puedes crear reportes específicos del contexto de las descargas. Digamos puedes llevar estadísticas de cuantas personas entran a la sección de descarga y como llegaron ahí y luego que hicieron ya estando ahí (desde cosas sencillas como over’s, clicks, posición del mouse, hasta tiempos de interacción) y como todas las páginas pueden ser diferentes lo increible es que se puede configurar el sistema de GA para cualquier tipo de proceso, eso es lo que lo hace un sistema increible.

Se pueden llevar medidas de meta unidas a sistemas de costo por click, con lo cual se puede hacer un verdadero estimado de cuanto se está ganando y cuanto se está gastando y así llevar una mejor administración y saber si hay un ROI positivo o no.

Y luego para ponerle una cereza en el pastel tiene un api para manipular todos los datos de la manera que uno lo quiera (alguna vez ya platiqué como esto se puede usar para generar contenidos según un perfil de los usuarios) con lo cual se pueden generar reportes en tiempo real sobre datos que no estén completamente a la vista.

Un gran sistema que invito a todos los webmaster que no lo conocen a probar.

Saludos,<br />
Gorka
