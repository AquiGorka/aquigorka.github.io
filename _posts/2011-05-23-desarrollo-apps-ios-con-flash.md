---
id: 20110523
title: Desarrollo apps iOS con flash
date: 2011-05-23T11:27:07+00:00
author: Gorka
layout: post
permalink: /2011/05/desarrollo-apps-ios-con-flash/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2011/05/cloud-computing.jpg" alt="Cloud Computing" />

Así que siguiendo con la línea de análisis y pruebas para desarrollo de apps para iPhone, iPod Touch y iPad me puse a hacer unas pruebas de código de un proceso que me tenía “preocupado” (preocupado porque si no lo podía hacer con el paquete de flash implicaría que hasta para aplicaciones “sencillas” sería completamente necesaria una Mac – pero no).

Una parte que me parece muy interesante/importante de los nuevos desarrollos (incluyendo pero no sólo limitado a apps) es que tengan la posibilidad de descargar contenido actualizable vía otros medios (es decir descargan noticias, novedades, resumenes, marcadores, etc. de servicios web) y para esto es necesario poder hacer una llamada estilo REST desde la aplicación.

Mi duda era si el paquete de iPhone developer de flash cs5 tendría acceso a este tipo de peticiones (REST – que implican desde GET, POST, XML, SOAP, JSON, etc. a un web service o simplemente un script de respuesta) y la verdad es que sí se puede y es MUY sencillo, tan sencillo que aquí pongo el código de una llamada estilo “hello world”:

```as3
var variables:URLVariables = new URLVariables("var_envio=valor_envio");
var request:URLRequest = new URLRequest();
request.url = "http://www.[mi_dominio].com/";
request.method = URLRequestMethod.POST;
request.data = variables;
var loader:URLLoader = new URLLoader();
loader.dataFormat = URLLoaderDataFormat.VARIABLES;
loader.addEventListener(Event.COMPLETE, completeHandler);
try{
  loader.load(request);
} catch(error:Error){
  trace("Unable to load URL");
}
function completeHandler(event:Event):void {
  trace(event.target.data.var1);
}
```

Así de sencillo y lo bueno es que se pueden envíar variables para toma de decisiones de operación/negocio. Cabe decir que la manera de recibir variables es en formato de variables HTML (par variable=valor). Listo, con este tipo de llamadas posibles se puede crear una app que se actualiza vía un servicio y que muestra nuevos contenidos cada que la persona la abre y también se puede guardar información del usuario en un servidor (datos de registro, de estado, de uso, etc.) y así hasta conectar con otros servicios que tengan que ver con la app (imaginen un juego que necesita que uses al mismo tiempo app y computadora por ejemplo, en fin…).

Saludos,
Gorka

P.D. – lo siguiente que voy a averiguar es si se puede abrir un socket a un servidor y así tener una línea abierta para apps estilo juegos de cartas / chats – todo esto obviamente desde flash cs5 y su sdk para iphone.
