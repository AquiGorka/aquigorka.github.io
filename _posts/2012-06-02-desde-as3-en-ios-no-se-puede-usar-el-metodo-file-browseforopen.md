---
id: 20120602
title: "Desde AS3 en iOS no se puede usar el método File.browseForOpen"
date: 2012-06-02T11:27:07+00:00
author: Gorka
layout: post
permalink: /2012/06/desde-as3-en-ios-no-se-puede-usar-el-metodo-file-browseforopen/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2012/06/not_gonna_happen_mug.jpg" alt="Not gonna happen mug" />

Así de sencillo, por ahora en Android si se puede pero no en iOS – el tema es que no se puede hacer revisión, así que hay que hacer algún tipo de hack para revisar si se puede o no.

```AS3
import flash.system.Capabilities;

if(Capabilities.os.indexOf(‘iPhone’) > -1){
  // código que cambia lo que haya que cambiar ya que no se puede usar browseForOpen
}
```

Referencia: https://books.google.com.ar/books?id=3NhBzZKpd80C&pg=SA6-PA52&lpg=SA6-PA52&dq=as3+ios+browseforopen&source=bl&ots=1lsfLBeaQK&sig=VFDNH9vp27FazuPgpozpwuELTxI&hl=en&sa=X&ei=kjbRT9iLL42Q8wTmi4Uf&redir_esc=y#v=onepage&q&f=false

Saludos,<br />
Gorka

P.D. – con este hack también pueden saber si están trabajando con iOS o con Android desde AS3

