---
id: 183
title: Nuevas Herramientas
date: 2017-05-28T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/05/nuevas-herramientas/
categories:
  - Ideas
---
<img src="/wp-content/uploads/2017/05/hand-tools.png" alt="Digital toolset" />

> <p style="text-align: right; font-style: italic;">
> La tecnología.<br />La tecnología ha de ser invisible para los usuarios. No tienes por qué entregar una lata de refresco con un drone si puedes entregarla en mano previamente, porque lo que importa es que el usuario tiene sed, no que tú tengas un drone.<br />Daniel Granatta
> </p>

No sé si estoy de acuerdo. Tampoco creo que estoy en desacuerdo.

Lo que pienso en ambos casos es así (está mezclado):

Creo que ese tipo de propuestas harían que no hubiera innovación por el gusto de hacer innovación. Para qué se necesita el drone si se puede entregar el refresco en mano, si la necesidad es la sed del usuario - pero y la necesidad de saciar la sed en un lugar al que se puede acceder mucho más rápido vía drone?

En la ciudad entregar refrescos con drone es un claro overkill, pero en zonas austeras donde no hay acceso a tiendas en cada esquina, ahí tiene sentido.

Entonces, entregar refrescos en drones tiene sentido sólo cuando existe la necesidad? Ahí es donde digo que no estoy de acuerdo, el hecho que se puedan entregrar refrescos con drones abre las puertas a repensar muchos otros lugares/necesidades donde se puede aplicar ese overkill de tecnología - lugares donde no es un overkill y donde el status quo no hacía/dejaba ver que había una necesidad, un problema a mejorar; y el uso de drones en otro lado por efímero que parezca puede ser un disparador de innovación en otro.

Un par de ideas para empezar el post. Ahora a las nuevas herramientas:

- Vim
- tmux
- shell (en realidad zsh)
- Go (y por ahí encontré Crystal tmb pero no lo usé aún)
- Docker/Vagrant

## Vim

Es lo más divertido. Es un editor de texto al estilo línea de comando, dónde escribir es sólo un modo y en realidad, todo lo que haces lo haces por comandos - para todos ya es común usar CTRL+V y CTRL+C para copiar y pegar, bueno Vim es así para todo, hay comandos y combinaciones de teclas para cada cosa (y las que no existen se pueden crear).

Tiene un _learning curve_ alto, pero te acostumbras y poco a poco lo usas para todo. Y lo divertido es que tiene plugins y una comunidad gigante haciendo mejoras constantemente. Hoy por hoy, mi editor of choice.

## tmux

Trabajando con Vim ahora de repente me la vivía acomodando ventanas por todos lados y tuve que buscar un tile manager para hacer eso de manera rápida. Luego aprendí que con Vim puedo tener varios archivos abiertos y trabajar entre ellos, así sólo necesito 1 ventana abierta al máximo y hacía el splitting desde Vim. Kapow!, llegó tmux (y es gracioso, uso tmux en iTerm que puede ser un overkill pero hay lugares donde no tengo iTerm así que de esta manera es todo una sola forma). En fin, tmux: una solo programa tamaño máximo y ahí mismo múltiples sesiones, es algo como múltiples escritorios dentro de un solo programa.

Muy cómodo y fácil de usar, y también todo configurable - apenas estoy aprendiendo qué y cómo para ver como lo defino a mi gusto personal.

## Zsh

Al estar usando Vim y tmux (y menos Sublime, Atom y Visual Studio) me encontré cada vez más trabajando con línea de comando, si bien ya instalaba y jugaba un poco con Zsh ahora empecé a configurar a mi gusto todo (desde alias, binarios propios, plugins e instalaciones automaticas). Y por supuesto Oh My Zsh - una comunidad de agregados super chulos para Zsh.

Los temas son muy cómodos y variados, y la idea es que con un dotfiles te puedes llevar esas configuraciones a todos lados facilmente (https://github.com/AquiGorka/dotfiles)

## Go

Aprendí a programar en C y luego C++. Nunca más los volví a ver, nunca los usé y no creo usarlos (nunca digas nunca). Pero de repente me crucé con un lenguaje que te ofrece la potencia, fuerza y velocidad de C pero con una sintaxis y con interfaces más sencillas de usar: Golang.

No jugué aún con los channels pero parece que para hacer sistemas que corren en paralelo ya viene optmimziado - genial!

Lo que si hice ya, y sigo haciendo es usar Go para mis servers de api (https://github.com/AquiGorka/kickoff/game) y viniendo de Node, la verdad es que es muy fácil hacer esto.

Luego encontré Crystal, que sería el Go para los que vienen de Ruby (yo vengo de Node) y plantea la misma idea: La fuerza y poder de C pero con la sintaxis sencilla y limpia de Ruby - no niego que me da curiosidad, pero por ahora no lo voy a probar, solo lo mantengo en el radar.

## Docker/Vagrant

Los casos de uso por los cuales ya estoy usando este tipo de programas (si es que los puedo llamar así, en realidad son virtualizaciones de software):

- Ambiente de desarrollo uniforme
- Simulación de ambientes de build
- Simulación de ambientes de producción (este en realidad aún no lo uso pero ya sé que si lo voy a hacer)

Para el primero: no me hace falta instalar las herramientas y programas para desarrollar si ya vienen en una imagen - para que instalar node, ruby, go, php, mysql, mongo, etc, etc. si puedo tenerlo listo en un ambiente virtualizado donde simplemente monto/comparto los archivos de mi máquina y los trabajo con mi editor de costumbre y listo.

Tampoco es overkill isntalar esos otros programas de desarrollo en mi máquina, lo acepto PERO que pasa cuando tienes versiones que chocan entre lo que quieres y lo que tienes - ejemplo las mac vienen con ruby y gem pero no puedes usarlo para desarrollos propios y no lo vayas a modificar porque si lo jodes, kapow! te llevas el sistema. Cómo se resuelve esto? Con *version managers*, que PAJA - un version manager de ruby, otro de node, otro de npm, nel. Ambientes virtualizados con las versiones que necesito y punto.

Para el segundo: estuve aprendiendo a hacer un continuos delivery desde bitbucket a google cloud engine (futuro post y código en github). Y pues qué más fácil que bajar la imagen de la máquina de bitbucket que hace el test y build y delivery, correrlo local y cuando todo funcionaba mandar el script a bitbucket y confirmar que todo seguía _ceteris paribus_.

Para el tercero: cuando lo haga lo cuento.


Así que bueno, ahí está un resumen rápido (pero no corto) de las herramientas que vengo aprendiendo y usando ultimamente - me faltaron otras: jekyll, hugo y github pages pero esas las contaré en otro post.

Saludos,<br />Gorka
