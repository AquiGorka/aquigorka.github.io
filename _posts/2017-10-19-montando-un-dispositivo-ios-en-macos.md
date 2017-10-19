---
id: 20171019
title: Montando un dispositivo iOS en MacOS
date: 2017-10-19T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/10/montando-un-dispositivo-ios-en-macos/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2017/10/hard-drive.png" alt="Hard Drive" />

Un post sencillo para poder usar la terminal y "navegar" en el dispositivo y sus archivos.


## Librerías

Instalar estas librerías (o verificar que ya lo estén) con `brew`:

- osxfuse
- ifuse
- lsusb


## Montar

0. `mkdir ios-device`
1. `lssub`
2. `idevicepair pair` // este va a dar el serial del dispositivo
3. `ifuse ios-device -u device_serial`
4. `ls ios-device`

Cuando terminen de usar el dispositivo:

4. `diskutil unmount ios-device`
5. `rm -rf ios-device`


## Posible error: `ifuse failed to connect to lockdownd service on the device`

Entrar [aquí](https://gist.github.com/samrocketman/70dff6ebb18004fc37dc5e33c259a0fc#gistcomment-2140745) para resolver.


### Referencias

- https://superuser.com/questions/465394/how-can-i-mount-an-iphone-as-a-drive-on-os-x/1135668#1135668
- https://gist.github.com/samrocketman/70dff6ebb18004fc37dc5e33c259a0fc


Saludos,<br />
Gorka
