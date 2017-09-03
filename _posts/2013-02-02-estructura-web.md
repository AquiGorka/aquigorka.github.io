---
id: 20130202
title: Estructura Web
date: 2013-02-02T11:27:07+00:00
author: Gorka
layout: post
permalink: /2013/02/estructura-web/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2013/02/webstr.gif" alt="Web Structure" />

Así que, con los años he ido cambiando de manera de trabajar, originalmente hacía unas cosas medio raras (había carpetas Controller, Model y View públicas), luego aprendí a poner las cosas en su lugar (folders no públicos), luego aprendí a usar htaccess para tener un solo controlador principal que se hace cargo de todas las peticiones (excepto fotos y archivos que sí existan – onda wp) y mi propio framework ha ido evolucionando.

Tanto me ha gustado con los años que lo empecé a usar para mis apps.

Despúes, con las apps y leyendo y tratando de usar otros frameworks (emberJS especificamente) aprendí a reacomodar y volvió a evolucionar el framework – lo fregón es que es flexible, tan flexible que se puede usar tanto para backend como para frontend (con sus respectivas modificaciones).

Así que, volviendo, ahora lo que quiero hacer es volver a mejorarlo y traerme los proyectos que usan versiones viejas (trota estoy hablando de ti) a la siguiente versión.

En esta nueva versión he estado pensando mucho el tema de html estáticos. En wp hay un plugin que transfomra los posts y pages a .html y eso genera una mejora sustancial en performance – igual que usar un cdn para archivos multimedia – y es obvio, ya no hay un script que tiene que ponerse a trabajar para escribir el html.

Lo que quiero lograr es que los html estáticos representen “estados” del website (sería la manera web 1.0) y luego una app en javascript sea la que tome el control (entra web 2.0).

El principal problema es que este esquema de html estáticos es muy poco flexible (MUY POCO). Qué pasa si quiero agregar un nuevo link a mi menú principal? Tendría que cambiar más de 650 html estáticos? Se puede hacer uno por uno con programa, pero no me parece óptimo, y luego si eso se tuviera que hacer cada 30 minutos? pierdes realmente las ventajas de performance que se habían ganado.

Me puse a buscar como hacer algún tipo de import o include en los html estáticos para ver si con eso podemos mantener un solo archivo y que todos los html lo incluyen, así se puede cambiar un solo archivo según lo que se necesite y todo se actualiza. Encontré que con el tag object se puede hacer esto, y hay muy poco escrito así que no es casi usado. Tengo que ver si este método funciona para cuidar seo y otros detalles, pero ya iré escribiendo lo que encuentre.

Saludos,<br />
Gorka

UPDATE – Aviso que las pruebas no son positivas. Ni con object, iframe, frame u embed – no hay manera que acepten el CSS del parent (y ni siquiera me he puesto a ver que onda con los links y el js). Pero existe una opción llamada Server Side Includes (que funciona en apache para exactamente este tipo de situaciones), quiero ver si en los cdn’s de cloud que quiero usar esto puede funcionar..

