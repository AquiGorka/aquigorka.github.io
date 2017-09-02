---
id: 20130201
title: Wifi Tarjeta Realtek y Linux (Debian Based)
date: 2013-02-01T11:27:07+00:00
author: Gorka
layout: post
permalink: /2013/02/wifi-tarjeta-realtek-y-linux-debian-based/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2013/02/realtek-chip.gif" alt="Realtek Chip" />

Medio que me estoy obligando a escribir este post (si no lo hago me voy a sentir muy mal y ya se que ‘luego’ no lo voy a escribir).

En algo que escribiré en un post después (si, ajá…) decidí aprovechar un disco duro que tenía por ahí sin usar. Decidí instalarle Windows y Linux (con la idea de ver si a través de Virtual Box podía usar Mac OS – y decidí el dual boot con windows porque mi hardware no daba para Xen con acceso directo a hardware). La parte de windows fue trivial (lo que me faltaba fue fácil encontrar ya que venía por default en mi otro disco duro, así que los drivers que faltaban los descargué directamente de Toshiba – windows 7). Para Linux escogí Debian (si les interesa saber porque me preguntan en los comments) y después de probar el LiveCD me mandé directo a ‘particionar’ y a instalar. Todo fluído hasta la parte del wifi, tuve que ir a conectarme por cable para tener Internet y así buscar cómo hacerlo funcionar.

Estuve toda la mañana de ayer y no logré nada. En resumen, varios links y foros donde decían que descargara los drivers de Realtek directamente para mi ‘chipset’ (que a su vez tenían que ser relacionados con mi kernel – y no se crean, mucho de esto también era griego para mí ayer – en un momento casi me lanzo a actualizarlo, pero luego vi que para arquitectura 64bits ya tenía la última versión – y que había que bajar el código fuente y compilarlo / otras opciones hablaban de agregar otro source descargar los headers de la versión y bajar el firmware y actualizar todo junto. Al bajar los drivers de realtek incluían un archivo con instrucciones para varios escenarios y un script que debía hacer las cosas correctamente – que no lo hizo y que además decía que justo con mi kernel hay problemas… pfff, de esas cosas que te ahuyentan. Ayer intenté todas esas opciones y nada, no pifaba.

Hoy decidí darle MUCHA lectura antes de hacer nada, con la ‘práctica’ del día anterior ya habría conceptos que no me dejarían con cara de ‘y si mejor bajo Ubuntu y a ver si ahí todo se hace por si mismo…’. Así que me leí todo un post ETERNO en un foro de gente con mi misma situación, intenté un par de opciones y luego como por arte de magia, pifó! y pifó bien, sin problemas de conexión y un tonel de otras posbiles situaciones que mencionan en el foro.

En resumidas cuentas (mis 2 centavos):

 -Descargar archivo de driver (creo que está parchado por la gente del foro). Es un ‘tarball’ o .tar.gz.
- Abrir en folder. Yo lo puse en user home por si hay que volver a hacer esto con actualizaciones de sistema operativo.
- apt-get install make (sólo por si lo no tienen, es para compilar).
- Abrir terminal y moverse al nuevo folder.

```sh
sudo su
make clean
make
make install
reboot
```

- modprobe rtl8192se_pci (aquí intenté con FN + F8 que es por hardware activar mi wifi, no está de más mencionarlo)

Espero ayude a quien tenga que ayudar.

```
Chipset : Realtek 8191SE
Laptop : Toshiba A505-S6005
Dirver : http://launchpadlibrarian.net/38201251/rtl8192se_linux_2.6.0014.0115.2010.tar.gz
```

Foro (ayuda MUY larga) : https://bugs.launchpad.net/ubuntu/+source/linux/+bug/401126?comments=all

Saludos,<br />
Gorka
