---
id: 20230917
title: "Snippets: input & paste"
date: 2023-09-17T00:00:00+00:00
author: Gorka
layout: post
permalink: /2023/09/snippets-input-copy-paste
categories:
  - Hacks
  - TIL
---

<img style="margin: auto;" src="/public/img/2023/09/dont-tread-on-me.jpg" alt="Don't tread on me" />

```js
const dontTreadOnMe = (e) => e.stopImmediatePropagation();
document.addEventListener('paste', dontTreadOnMe, true);
```

A mi me pasa en un par de websites que cuando quiero pegar la contraseña parece ser que lo deshabilitaron, este snippet permite deshabilitar la deshabilitación - ja!

[Fuente](https://twitter.com/fireship_dev/status/1698438648549802104?s=43&t=_BmPaSNdfbfIxTQoNSYLhg)

Saludos,<br />
Gorka
