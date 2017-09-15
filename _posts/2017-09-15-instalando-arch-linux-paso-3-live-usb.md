---
id: 20170915
title: "Instalando arch linux: Paso #3 Live usb"
date: 2017-09-15T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/09/instalando-arch-linux-paso-3-live-usb/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2017/09/antergos-live-usb-drive.jpg" alt="Antergos live usb" />

Aparentemente este fue muy fácil, pero aún no lo pude comprobar y ya me ha pasado antes que al tratar de hacer un live usb con alguna distro de linux en Mac no funciona. Esta vez cambié al forma de hacerlo con las instrucciones de esta [web](https://wiki.archlinux.org/index.php/USB_flash_installation_media#BIOS_and_UEFI_bootable_USB), que acá explico:

- En una terminal escribir `diskutil list` para ver la lista de dispositivos.
- Descrifrar cuál es el usb (sí, el usb tiene que estar conectado), normalmente tiene estas características `/dev/disk2 (external, physical)`.
- Desmontar el usb `diskutil unmountDisk /dev/diskX` <- OJO cambiar la X por el número correcto.
- Copiar la distro live al usb con `sudo dd if=path/to/arch.iso of=/dev/rdiskX bs=1m` <- hay una `r` antes del disco esa es importante y OJO cambiar la X también.
- Al terminar la Mac puede advertir `The disk you inserted was not readable by this computer` simplemente seleccionar ignore y listo.

Esperemos que todo funcione y que no tenga que hacer otro post de como hacer esto correctamente.

Saludos,<br />
Gorka
