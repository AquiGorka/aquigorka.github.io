---
id: 20171024
title: Cloudflare
date: 2017-10-24T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/10/cloudflare/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2017/10/cloudflare.jpg" alt="Cloudflare" />

¿Cómo tener SSL (gratis) para mis websites?

Una opción que estoy por probar es la empresa [Cloudflare](https://www.cloudflare.com/). Los pasos a seguir en el setup son bastante sencillos:

0. Crear una cuenta

1. Scan

Hay que definir el website que se va a usar y ellos hacen un primer scan de los settings DNS.

2. Revisión DNS Records

Si no se han usado estos settings lo más probable es que todo esté correcto. Si se agregaron subdominios o entradas específicas sólo hace falta revisar que están bien.

3. Plan

Hay varios, en mi caso fui por el Free Plan.

4. DNS

Te listan los nameservers a los que debe apuntar tu dominio.

5. Overview + Check

Una revisión general de todo y te avisan si el cambio de DNS se hizo correctamente (esto puede llegar a tardar en lo que el cambio se distribuye).

6. Crypto

Aquí viene lo bonito, hay que buscar las siguientes entradas y cambiarlas a las siguientes configuraciones:

- SSL en la opción: Flexible
- Always use HTTPS: sí
- Automatic HTTPS Rewrites: sí


Y BOOM. Listo. Website con SSL, es decir, website con `https` al principio.

Cabe avisar que en realidad lo que se está haciendo aquí es que el "resto del mundo" va a acceder de manera segura a los servidores DNS de Cloudflare y que ellos van a regresar la información del website solicitado pero si no hay SSL en el website esta comunicacion (la de Cloudflare pidiendo la información) se hace sin SSL.

Bueno, bonito y barato. Ya les contaré como me fue.

Saludos, <br />
Gorka




