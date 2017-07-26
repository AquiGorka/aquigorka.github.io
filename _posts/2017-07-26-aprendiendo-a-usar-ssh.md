---
id: 20170726
title: Aprendiendo a usar ssh
date: 2017-07-26T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/07/aprendiendo-a-usar-ssh/
categories:
  - Ideas
---

<img style="margin: auto;" src="/public/img/2017/07/ssh.jpg" alt="ssh" />

> <p style="text-align: right; font-style: italic;">Secure Shell (SSH) is a cryptographic network protocol for operating network services securely over an unsecured network. The best known example application is for remote login to computer systems by users.<br />
<a href="https://en.wikipedia.org/wiki/Secure_Shell">ssh @ Wikipedia</a></p>

## ssh

Eso, la aplicación más conocida es para conectarte de manera segura con otras computadoras. Esto puede ser desde la terminal o con otros programas que usan ssh con algún tipo de interfaz gráfica.

Hay dos programas:

- cliente
- servidor

El cliente se conecta al servidor. Es decir, se necesita una computadora que tiene algún servidor ssh corriendo - en mi caso, he usado openSSH pero hay más. Seguramente que se puede tener el cliente en la misma computadora que tiene el servidor pero aún estoy aprendiendo así que hagamos esto fácil y paso a paso.

**Para los siguientes ejemplos tengo un servidor corriendo en user@ip.de.servidor**

### ssh -L

Sirve para hacer un tunel en un puerto local hacia algun otro lugar via el servidor definido.

```sh
ssh -L 9000:localhost:8888 user@ip.de.servidor
```

Al entrar yo (en cualquier browser) a http://localhost:9000 lo que voy a ver es lo que regresa el localhost de la computadora corriendo el openSSH (server de ssh) en el puerto 8888.

También podría apuntar a cualquier otro lugar del mundo (eg www.google.com:80) pero no logré un ejemplo que funcionara (me mandaban paginas 404 supongo que por error de configuración local a la petición via localhost).


### ssh -R

Sirve para hacer un tunel a un puerto remoto de un puerto local, es decir, lo que se tenga en mi computadora (que por ahora es el cliente ssh) se va a ver en la computadora remota (la que tiene el server ssh y en el puerto definido).

```sh
ssh -R 9090:localhost:8080 user@ip.de.servidor
```

Esta opción está rebuena para desarrollo en dos casos específicos (ambos casos necesitan que la computadora con el server ssh sea accesible via web):

- acceso a desarrollo local desde otra computadora (como un cliente) - así se le puede mostrar a terceros lo que se está trabajando sin que estén en el mismo lugar físico.
- accesso a desarrollo local desde mobile - así puedo probar cambios y nuevos features directamente en los dispositivos


### ssh -D

La última por hoy, y una muy divertida: sirve para usar la computadora con el server ssh como proxy para las peticiones locales - hay que hacer una configuración más local, hay que decirle al OS o al browser o a curl (ver ejemplo abajo) que use socks5 proxy para los requests.

Esto está muy divertido ya que ahora tenemos una VPN (por ahora de emergencia, y siguiendo las recomendaciones que me han hecho, si quieres una VPN lo mejor que puedes hacer es pagar por una VPN).

```sh
ssh -D 9002 user@ip.de.servidor

curl --socks5 localhost:9002 www.aquigorka.com
```

Así que ahí está, ya iré aprendiendo más y compartiendo como hacer más cosas.

Saludos,<br />
Gorka

