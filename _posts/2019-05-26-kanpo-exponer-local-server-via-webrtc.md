---
id: 20190526
title: "Kanpo: exponer local server via WebRTC"
date: 2019-05-26T21:03:07+00:00
author: Gorka
layout: post
permalink: /2019/05/kanpo-exponer-local-server-via-webrtc/
categories:
  - Ideas
---

<img style="margin: auto;" src="/public/img/2019/05/limits.png" alt="Límites" />

Hace unos días me pasó algo curioso: ayudando a un amigo hicimos un "puente" usando `ngrok` a su servidor local (nada raro hasta aquí), después de un par de peticiones empecé a recibir mensajes de error por parte de `ngrok`, decía que me estaba pasando del límite requests - `ngrok` mismo dice que es raro que te vayas a pasar:

>Limits are imposed on connections, not requests. If your HTTP clients use persistent connections aka HTTP keep-alive (most modern ones do), you'll likely never hit this limit.
>
> https://ngrok.com/pricing

Pero pasó. Y me vino la idea de usar WebRTC (como ultimamente me pasa, WebRTC para todo).

De ahí nació [`Kanpo`](https://github.com/AquiGorka/kanpo) - aviso, es un _work in progress_.

Las ventajas de usar esta herramienta contra los servicios que usan servidores para comunnicar la data son 1) WebRTC por default usa `ssl`, entonces las comunicacione están cifradas y no pueden espiar; 2) No se usa un punto central que puede fallar, es decir, no dependes de un servicio que hoy funciona y quien sabe como siga mañana; y 3) No hay que pagar para evitar que limiten los datos que van a estar pasando por sus servidores lo que abre la puerta a 4) Se pueden mandar miles y miles de requests por segundo si así se quiere.

Aca les dejo un par de opciones "conocidas" para exponer servidores locales que usan servidores de _relay_ (en lo que funciona `Kanpo`):

- [`ngrok`](https://ngrok.com/)
- [`localtunnel`](https://localtunnel.github.io/www/)

Ya iré avisando cuando `Kanpo` vaya siendo actualizado y funcional.

Saludos,<br />
Gorka
