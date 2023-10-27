---
id: 20231027
title: "Como cambiar audio source con el teclado"
date: 2023-10-27T00:00:00+00:00
author: Gorka
layout: post
permalink: /2023/10/como-cambiar-audio-source-con-el-teclado
categories:
  - Hacks
  - Life pro tips
  - Automations
---

<img style="margin: auto;" src="/public/img/2023/10/select-source.jpg" alt="Select source" />

El cuento corto es que cada tanto uso los speakers de la compu pero a veces necesito cambiar a los auriculares y viceversa. Antes, lo hacía con los system settings de audio escogiendo el output deseado. Para esto tenía que traer spotlight/alfred `CMD + Spacebar` y escribir `sound` (cuantas veces me equivoqué por escribir rápido con `soud` sólo para tener que borrar la `d` y escribir la `n`) y con el mouse escoger la salida que quería.

No más.

Ahora hago `CMD + Shift + H` para los auriculares y `CMD + Shift + M` para los speakers.

¿Cómo?

Con un par de _goodies_:

- [`switchaudio-osx`](https://github.com/deweller/switchaudio-osx): instala `SwitchAudioSource`.
- [`Script kit`](https://www.scriptkit.com/): que instala un  programa para hacer _muchas_ cosas, que por ahora yo uso para hacer keyboard shortcuts.

`SwitchAudioSource` es el programa que deja cambiar la salida de sonido desde la terminal y con `Script kit` puse los shortcuts para las dos acciones que contaba arriba.

Igual, como me gusta mucho de hacer alias tengo unos cuantos alias para usar `SwitchAudioSource` (porque quien va a escribir todo eso!):

```sh
alias shead="SwitchAudioSource -s \"External Headphones\""
alias smac="SwitchAudioSource -s \"MacBook Pro Speakers\""
alias sall="SwitchAudioSource -a"
alias scur="SwitchAudioSource -c"
```

Y con eso, los scripts finales para `Script kit` quedaron en:

```sh
// Name: Shortcut to Headphones
// Shortcut: cmd shift h

import "@johnlindquist/kit"

await $`/bin/zsh -lic shead`
```

y

```sh
// Name: Shortcut to Speakers
// Shortcut: cmd shift m

import "@johnlindquist/kit"

await $`/bin/zsh -lic smac`
```

Saludos,<br />
Gorka
