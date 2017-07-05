---
id: 214
title: Aplicaciones, sistemas y web
date: 2010-12-31T11:27:07+00:00
author: Gorka
layout: post
permalink: /2010/12/aplicaciones-sistemas-y-web/
categories:
  - Ideas
---
<img style="margin: auto;" src="/wp-content/uploads/2010/12/apps.png" alt="Apps" />

Como parte del desarrollo de aplicaciones, sistemas, páginas, etc. que funcionan en Internet una de las principales partes es escoger un sistema de hosting.

Los sistemas de hosting vienen también en una gran gama de sabores y colores: linux + apache; java + weblogic , + wea, + tomcat; windows + IIS, etc.etc. y por supuesto cada una de estas opciones tiene acceso a diferentes lenguajes de scripting (php, python, jsp, perl, ruby, asp, etc.) y por lo tanto es un tema importante a la hora de decidir cuál escoger (y esto aún si hablar de bases de datos y sus manejadores).

Los hosting típicos hoy en día manejan de base algún linux y te dejan usar php o python con base de datos mysql. Te cobran una anualidad por espacio en disco y uso de ancho de banda. Los servidores se comparten para “amortizar” su costo entre diferentes clientes, lo que hace que muchas veces se pueda abusar de los recursos que se tienen y sean otros los que sufren las consecuencias (cuando se atora un servicio en un servidor compartido todos los demás clientes en ese servidor dejan de tener acceso a tal servicio). Los costos típicos de estos servicios van desde $15 a $400 dólares anuales (además que ya incluyen toda una suite de aplicaciones para administrar los servicios de email, ftp, bases de datos, etc).

Como consecuancia a los posibles abusos en los hostings “compartidos” se crearon los “VPS” o servidores virtuales privados en los cuales se paga por tener un acceso garantizado y “limitado a” a los recursos del servidor en versión virtual, con esto se tiene un servidor dedicado para mi sistema, aplicación ó página web pero “pequeño y limitado” (un servidor dedicado varía pero puede llegar hasta $4,000 dólares anuales) que ronda los costos de $20 a $250 dólares mensuales. Además en con un VPS tienes acceso de usuario (telnet, ssh, etc) a tu cuenta, cosa que no se puede en un servidor compartido, y así puedes instalar software y paquetería que no está preinstalada en los paquetes compartidos.

Desde hace ya un par de años vengo leyendo de otra tendencia en cuanto a opciones de hosting (por así llamarlo) y es usar **“Cloud Services“**. Esto quiere decir que en una red de servidores que ya tienen un framework, arquitectura y estructura fijas y óptimas (estamos hablando  de big players como son Amazon, así que puedo asegurar que sus estructuras son de la mejor calidad). Lo que se ofrece en este tipo de servicios es hacer un uso de recursos por recurso y se cobra por recursos usados. Digamos que al guardar 1 mega de información al mes que fue solicitada 1 mega de ocasiones y para entregarla se usaron recursos del servidor (en la medida de recursos que no recuerdo) eso es lo que se te cobra al final del mes (y son costos MUY bajos). La gran ventaja de este tipo de servicios es que tienes a empresas grandes usándolas, así  que literalmente puedes decir que usas la misma arquitectura que ellas y cuando te dicen que el uptime es de 100% no es una manera de venderte el servicio (esto porque muchas de las empresas de hosting compartido te dicen que van a tener uptime el 99.99999% del tiempo y a la mera hora no es cierto y luego sus servicios a clientes están de vacaciones también, pero bueno, hahaha).
La desventaja de este tipo de servicios (específicamente el AWS de Amazon) es que para entrarle hay que tener conocimientos técnicos de uso y configuración de servicios en servidores más avanzados y cuando tu estrategia es entregar servicios/contenidos a la de “ya”, pelearte por configurar los servicios de Amazon se entiende como tiempo perdido y pues las soluciones “compartidas” resultan más cómodas.

Hace unos días me encontré con el Google App Engine, es una propuesta similar al AWS de Amazon para Cloud Services y me pareció muy interesante, me puse a leer y ví que no es tan difícil usarlo y me puse a averiguar más, resulta que sí tiene sus problemas:

- de entrada, sólo acepta JAVA (y sus derivados como Ruby) o Python como lenguajes de desarrollo
- no usa Bases de Datos Relacionales (orale! ya que explican que un JOIN es maligno y poco eficiente entre servicios en diferentes servidores) así que hay que aprender a usar su sistema de administración de datos (no lo he usado pero lo que explican es que se entiende como una gigante hash table)
- tiene un sistema de prueba gratuito (esto no es malo, pero…) con limites bajos de uso: 500 megas de espacio, 10,000 peticiones diarias, máximo mil archivos (igual todos estos límites se pueden liberar pagando)

La verdad es que le voy a dar oportunidad a estos servicios por la parte de usabilidad e introducción. A diferencia de Amazon con estos directamente puedo descargar un SDK (paquetería de desarrollo) para empezar y ver como va funcionando. Por ahí me voy a tener que forzar a reparender JAVA, lo cual hasta suena divertido (o MUY nerd, hahaha) y ver como hacerle con las limitantes de base de datos pero las ventajas de tener un sistema de frente que use los servicios de Google me parece bastante atractivo, igual estaré usándolo para sistemas de backend de apps de iphone o hasta de apps de facebook y así no me tendré que estar peleando con mi hosting compartido para poder usar sockets (para multiplayers en tiempo real) y otros softwares (a ver si así ya puedo usar LISP o PROLOG y por fin crear mi app de “jugar al dominó”). Así que bueno, les iré avisando.

Saludos,<br />
Gorka
