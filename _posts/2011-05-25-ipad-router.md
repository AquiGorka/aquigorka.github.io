---
id: 20110525
title: iPad router
date: 2011-05-25T11:27:07+00:00
author: Gorka
layout: post
permalink: /2011/05/ipad-router/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2011/05/ipad.jpg" alt="iPad" />

Lo primero que tengo que decir es que aún no pruebo esto personalmente pero que en cuanto consiga mi plan de datos (vía 3G) lo llevaré a cabo y ahí les diré si era tan fácil como aqui lo voy a poner.

La idea general es así: con el iPad 3G (o con un iPhone y eventualmente si sacan un iPod Touch con 3G) se puede usar la señal de internet de la red de celular y compartirla con computadoras y otros gadgets (iPod Touch, etc.) así ya no se puede tener una red wifi que va contigo a todos lados (donde vaya el iPad o iPhone por supuesto).

Aunque los pasos suenan difíciles la verdad es que no lo son, primero los listaré y luego los explicaré:

1. Se necesita instalar una aplicación del tipo iProxy (no la iProxy que está en la appStore porque esa no es..) en el iPad. Este paso es el más difícil.
2. Crear una red con Ad Hoc con una computadora y conectar el iPad a la misma. Luego, desconectar todos los aparatos excepto el iPad.
3. Configurar el iPad para que sirva como router
4. Iniciar la app iProxy y configurarla
5. Conectar cualquier otro gadget a la red wifi y configurar su IP
6. Configurar un proxy para el gadget que se conecta (es solo una dirección en una forma no hay que aprender de esto)
7. Navegar

Ahora para la parte más detallada:

1. Instalar iProxy, lo que pasa es que se necesita una versión personalizada de iProxy para hacer esto ya que Apple no permite esta app así libre en la appStore, entonces hay que conseguir el codigo fuente, compilarlo e instalarlo. Esto se puede hacer directamente si se tiene cuenta de desarrollador de apps o con algún amigo que lo sea.
2. Esta parte es casi trivial y preferiría que busquen como hacerlo en Google (si no lo encuentran díganlo y lo pongo aqui)
3. Esto se logra configurando una IP fija de 10.0.0.1 y una mascara de red de 255.255.255.0 en el iPad
4. Debe de tener la IP fija que pusimos en el punto anterior y el puerto 8888 (tráfico de Internet)
5. Se puede seleccionar cualquier IP pero para rápido ejemplo ponerle 10.0.0.8 y submáscara de red de 255.255.255.0
6. Ya sea en el navegador o en el mismo firewall de windows o vía un http proxy se configura la dirección del mismo a: http://10.0.0.1:8080/socks.pac
7. Abrir alguna dirección web y comprobar que todo funcione.

Estuve leyendo que hay programas que se conectan a Internet sin usar tal configuración de proxy (Skype, etc.) entonces para eso se puede usar un programa de http proxy como Polipo para que todo el tráfico de Internet se canalice por ahí.

Así que bueno, se ve fácil, ya les diré como me va.

Saludos,<br />
Gorka

Aui les dejo links de referencia:

- http://www.google.com/search?sourceid=chrome&ie=UTF-8&q=ipad+share+3g+internet+connection#sclient=psy&hl=en&source=hp&q=ipad+iproxy&aq=f&aqi=g1&aql=&oq=&pbx=1&bav=on.2,or.r_gc.r_pw.&fp=c9ba145ff8753b37
- http://www.avforums.com/forums/ipad-ipad-2/1241501-iproxy-ipad-tethering.html
- http://andre.arko.net/2010/04/04/ipad-internet-via-iphone-without-jailbreaking/
- http://www.memention.com/blog/2010/05/15/Removing-a-step.html
- http://andre.arko.net/2010/04/04/ipad-internet-via-iphone-without-jailbreaking/
- http://vafer.org/blog/20100120001443/
- https://github.com/tcurdt/iProxy/wiki/
- http://www.youtube.com/watch?v=RQxKcJzbhac


