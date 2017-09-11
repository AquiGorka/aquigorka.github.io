---
id: 20170911
title: Instalando arch linux: Paso #1 rEFInd
date: 2017-09-11T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/09/instalando-arch-linux-paso-1-refind/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2017/09/refind.jpg" alt="rEFInd" />

Para poder hacer el dual boot se necesita poder escoger qué sistema operativo se va a usar, para esto entra [rEFInd](http://www.rodsbooks.com/refind/).

Esta parte no fue difícil, hay un tema de algo llamado [SIP](http://www.rodsbooks.com/refind/sip.html) (System Integrity Protection) por lo que hay que hacer un cambio rápido a la Mac en "Modo Recovery":

- Reiniciar la computadora
- Cuando se eschucha el "chime" apretar CONTROL + R
- En modo recovery aparece una ventana con 4 opciones - no hacer caso, en lugar ir al menú superior y en la opción Utilities seleccionar terminal
- Escribir `csrutil disable` y apretar enter
- Reiniciar

No es nada del otro mundo y se puede regresar al modo anterior con los mismos pasos pero cambiando el comando por `csrutil enable`.

Después de eso, en el usuario normal buscar la manera con la que uno se siente más cómodo para obtener rEFInd [acá](http://www.rodsbooks.com/refind/getting.html) (en mi caso fue el zip porque no encontré el archivo para instalar en el repo) y ejecutar el archivo con `./refind_install`. Reiniciar - en esta ocasión ya tendremos que seleccionar el SO desde rEFINd.

Saludos,<br />
Gorka
