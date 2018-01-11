---
id: 20180111
title: Usando Jekyll en Mac
date: 2018-01-11T11:27:07+00:00
author: Gorka
layout: post
permalink: /2018/01/usando-jeyll-en-mac/
categories:
  - Ideas
---

<img style="margin: auto;" src="/public/img/2018/01/jekyll.png" alt="Jekyll" />

Alguna vez ya hablé de [esto](https://aquigorka.com/2017/05/nuevas-herramientas/), resulta que para usar [Jekyll](https://jekyllrb.com/) se necesita tener instalado Ruby. Las Macs ya lo tienen por default así que debería ser fácil no? Pues no.

```sh
gem install jekyll
```

Me regresaba algo de `Permission Denied`. Puf. Entre las soluciones comunes siempre salía eso de usar un Ruby Version Manager (rvm). Me niego. Y de repente, esto: [Troubleshooting jekyll: Jekyll & Mac OS X 10.11](https://jekyllrb.com/docs/troubleshooting/#jekyll--mac-os-x-1011). Fiesta.

La solución implica instalar Ruby usando `Hombrew` (`Hombrew` es una fiesta en sí, luego hago un post de eso) y agregar ese ejecutable al `$PATH` del usuario, con eso tenemos la última versión de Ruby lista para usar y, consecuencia, se puede instalar Jekyll.

De ellos mismos:

>Either of these approaches are useful because /usr/local is considered a “safe” location on systems which have SIP enabled, they avoid potential conflicts with the version of Ruby included by Apple, and it keeps Jekyll and its dependencies in a sandboxed environment. This also has the added benefit of not requiring sudo when you want to add or remove a gem.

Perfecto y sin preocupaciones.

Espero les sirva.

Saludos,<br />
Gorka
