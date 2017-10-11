---
id: 20171011
title: "Instalando arch linux: Paso #6 primer intento fallido"
date: 2017-10-11T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/10/instalando-arch-linux-paso-6-primer-intento-fallido/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2017/10/error_grub.png" alt="Grub Prompt" />

**¿Qué puede salir mal?**

Muchas cosas. Y entre ellas que hagas click en instalar después de _creer_ que lo configurado está bien y que, al terminar la computadora pida reiniciar y te encuentres con una pantalla como la de arriba.

¿Qué diablos se hace con algo así?

Google. Más Google. Mucho más Google.

Y aún así, la respuesta no existe. La respuesta hay que encontrarla.

Esste era el error original:

```
ERROR: device 'UUID=xxx' not found. Skipping fsck
mount /new_root can't find UUID=xxx
You are bing dropped into an emergency shell
sh: can't access tty; job control turned off
```

Y desde el shell de emergencia poco pude hacer/investigar/aprender. Esta [referencia](https://unix.stackexchange.com/questions/364439/how-to-manually-boot-arch-linux-from-preboot-emergency-shell) proponía hacer esto:

```
# emergency shell
mount /dev/sda /new_root
exit
```

Nada.

Pero antes de llegar al shell de emergencia la computadora pasaba por `Grub` y podía detener el boot inicial y desde ahí mismo cambiar/configurar ese primer proceso:

```
ls
(hd0) (hd1) (hd1, gpt4) (hd1, gpt3) (hd1, gpt2) (hd1, gpt1)
ls (hd1,4)  # this is where I installed Antergos
Partition hd1,4: Filesystem type ext*
ls (hd1,4)/
lost+found boot var etc proc sys dev run tmp usr bin home lib lib64 mnt opt root sbin srv
```

Nada.

Buscando, viendo y tocando, no logré nada, decidí tratar de iniciar la compu de vuelta con el usb - no iba a pasar así como así. Traté de iniciar de esta manera:

```
#grub prompt
set root=(hd0) # este era el usb
linux /arch/boot/vmlinuz root=/dev/sda
```

En un momento detuve el boot inicial con el usb en la computadora y algo se vio diferente o algo se me ocurrió, y encontré la solución:

```
set root=(hd0,2) # aquí en el usb estaba la partición efi
chainloader /efi/boot/loader.efi
```

Y kaboom! El loader del usb con las opciones que tenía cuando iniciaba el cd live de Antergos.

Espero esto sirva a alguien en algún momento, y si no, por lo menos me queda de notas para el futuro.

Saludos,<br />
Gorka
