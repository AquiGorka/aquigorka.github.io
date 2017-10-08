---
id: 20171008
title: "Instalando arch linux: Paso #5 Internet en el live usb"
date: 2017-10-08T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/10/instalando-arch-linux-paso-5-internet-en-el-live-usb/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2017/10/-wifi-sleep.gif" alt="Antergos live usb + Internet" />

Siguiendo con todo esta fiesta ahora toca hacer que la Macbook Air tenga Internet, cosa que no es trivial ya que el live usb de Antergos no tiene los programas para usar el WiFi de la computadora (por que? supongo que no es trivial el tema de drivers y no es 1 solo programa entonces es más fácil no incluirlos y que cada quien se encargue).

Y para qué se necesita el WiFi? La gente de Antergos no quiere que se pueda instalar un sistema desactualizado, su filosofía es que cada instalación descarga lo necesario para estar al día.

Hay dos maneras:

- Un convertidor de cable ethernet a usb (porque las Macs no tienen puertos ethernet). Y con este puedo conectar la computadora directo al router.
- Vía el iPhone hacer tethering vía usb. OJO - no comparte el WiFi así que las descargas van a ser del plan de datos (y fueron ~700 megas en mi caso).

Pasos para lograr/configurar el iPhone tethering con la Macbook Air con el live usb de Antergos (usando como referencia [esto](https://alexeyzabelin.com/arch-on-mac)):

1- Descargar los siguientes programas, llevarlos en un usb a la computadora con Antergos:

- [ifuse](https://www.archlinux.org/packages/community/x86_64/ifuse/)
- [fuse](https://www.archlinux.org/packages/extra/x86_64/fuse/)
- [libimobiledevice](https://www.archlinux.org/packages/extra/x86_64/libimobiledevice/)
- [libusbmuxd](https://www.archlinux.org/packages/extra/x86_64/libusbmuxd/)
- [libusb](https://www.archlinux.org/packages/core/x86_64/libusb/)
- [libplist](https://www.archlinux.org/packages/extra/x86_64/libplist/)
- [libxml2](https://www.archlinux.org/packages/extra/x86_64/libxml2/)
- [usbmuxd](https://www.archlinux.org/packages/extra/x86_64/usbmuxd/)

2- En Antergos: montar si es necesario el usb, desde terminal ir al usb/folder donde están esos archivos y con cada uno hacer `pacman -U ARCHIVO`, cuando pregunte si queremos instalar/usar espacio poner `Y`.
3- En el iPhone habilitar el `Mobile Hotspot` y conectarlo por el cable usb a la computadora.
4- Para mi fue suficiente con hacer `idevicepair pair` la primera vez y Antergos reconoció la conexión y podía usar Internet, en la segunda ocasión tuve que hacer el paso 5.
5- `ip link` y con la interfaz que se ve hacer `dhcpcd INTERFAZ` y ahora sí, Internet funcionó.

Así que bueno, espero esto les funcione.

En el siguiente post ya vendrá el proceso de instalación en sí.

Saludos,<br />
Gorka
