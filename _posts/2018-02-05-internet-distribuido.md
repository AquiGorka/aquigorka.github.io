---
id: 20180205
title: Internet distribuido
date: 2018-02-04T11:27:07+00:00
author: Gorka
layout: post
permalink: /2018/02/internet-distribuido/
categories:
  - Ideas
---

<img style="margin: auto;" src="/public/img/2018/02/internet-of-things.jpg" alt="Internet of Things" />

>...demonstrating that decentralization is about much more than just controlling our own data. It is a fundamental rethinking of the relation between data and applications, which—if done right—will accelerate creativity and innovation for the years to come.
><br />
>[Paradigm shifts for the decentralized Web](https://ruben.verborgh.org/blog/2017/12/20/paradigm-shifts-for-the-decentralized-web/)

## ¿Qué es el Internet Distribuido?

El concepto viene recuperando fuerza desde hace tiempo ya. Cuando las redes sociales actuales se convirtieron en lo que son–hay que recordar épocas donde los anuncios que veíamos en redes sociales no tenían que ver con conversaciones que habíamos tenidos en voz alta–y nos dimos cuenta que somos el producto y no los usuarios. De repente, nos fuimos dando cuenta que las compañías son dueñas de nuestros contenidos, que compartimos libremente toda nuestra vida online y que esa información se la envíamos a una compañía sin ningún problema, y esa compañía **monetiza** nuestra data.

Un Internet distribuido significa que cada persona se responsabiliza por sus datos. Que cada persona es un nodo que se conecta al resto de nodos, en lugar de todos conectarnos a un nodo central–el cual dice qué, cómo, dónde, quién si, quién no, por qué y más, es decir, define las reglas del juego.

El Internet distribuido tiene que ver con recuperar el poder o, "empoderizar" (empower) de vuelta al usuario.

## ¿Cómo hacemos eso?

Hay muchos proyectos que ya lo están trabajando. Como parte de un proyecto interno en Citrusbyte he tenido la oportunidad de investigar las plataformas actuales con sus protocolos/herramientas. Entre las plataformas que investigamos están:

- [IPFS](https://ipfs.io/)
- [DAT](https://datproject.org/)
- [Scuttlebutt](https://www.scuttlebutt.nz/)

Cada uno con un acercamiento diferente. Nosotros nos decidimos en este proyecto por IPFS. Ellos ofrecen toda la _suite_ de herramientas para trabajar con sus protocolos (en estado _alpha_ con alto potencial de bugs y errores, algunos de los cuales describí [aquí](http://bits.citrusbyte.com/the-state-of-frontend-development-with-IPFS-in-2017/)).

## ¿Qué implica esto para los usuarios?

No mucho, aunque todo. Desde el lado de desarrollo hay que entender la manera en la que las nuevas estructuras se utilizan y como encuadran dentro de la arquitectura de una aplicación, y lo que se busca es que la UI no tenga cambios, es decir, que se pueda usar la Dapp (aplicación distribuida) sin ningún cambio, sin tener que aprender nada nuevo–con la diferencia que hay por atrás.

Lo que sí hay que entender es que los datos son del usuario, y que se necesita una computadora prendida y online para transmitir esos datos. De ahi que es importante para los desarrolladores ofrecer estrategias de redistribución de contenidos eficiente y sustentable (dependiendo de cada Dapp).

## ¿Cómo seguimos?

Sigan atentos, cuando el proyecto esté listo ya avisaré por aquí. Así podrán tener una primera interacción con estas tecnologías. Y luego, ya iré escribiendo posts de las nuevas herramientas que acompañan este tipo de proyectos.


Saludos,<br />
Gorka

Más información:

- http://blog.archive.org/2015/02/11/locking-the-web-open-a-call-for-a-distributed-web/
- https://ipfs.io/ipfs/QmNhFJjGcMPqpuYfxL62VVB9528NXqDNMFXiqN5bgFYiZ1/its-time-for-the-permanent-web.html
- https://webfoundation.org/2017/03/web-turns-28-letter/
- https://en.wikipedia.org/wiki/Distributed_computing
- https://www.ideou.com/blogs/inspiration/blockchain-and-distributed-web-why-you-should-care
