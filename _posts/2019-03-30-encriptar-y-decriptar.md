---
id: 20190330
title: Encriptar y decriptar
date: 2019-03-30T21:03:07+00:00
author: Gorka
layout: post
permalink: /2019/03/encriptar-y-decriptar
categories:
  - Ideas
---

<img style="margin: auto;" src="/public/img/2019/03/encrypt-decrypt.jpeg" alt="Encriptar y decriptar" />

He esstado leyendo y tratando de aprender como encriptar y luego decriptar información de manera segura (y tal vez algún día pueda decir: en la manera correcta).

Sin entrar a detalles que podrían mandarme por un agujero de conejo, describo lo que quiero hacer y luego lo que he encontrado:

Contexto:

- Se usa una llave privada y una llave pública (correspondientes)
- La llave privada la tiene una webapp
- La llave pública la tiene un servidor

El proceso:

1. La webapp hace un request a un primer endpoint (algo así como `/knock`)
2. El servidor recibe el request y genera una frase de manera random, entonces cifra la frase con la llave pública, guarda un hash de la frase y envía el texto cifrado como respuesta
3. La webapp recibe el `challenge`, lo decifra usando la llave privada y entonces genera un hash (usando el mismo proceso que el servidor para generar el hash) y manda al server el hash al siguiente endpoint (algo como `/answer`)
4. El servidor recibe los datos y compara los hashes, si son iguales entonces sabemos que la webapp tiene la llave privada correspondiente a la llave pública usada para cifrar el `challenge`

Para facilidad saqué otros puntos del proceso, pero esto describe la parte núcleo a resolver.

Encontré varias librerías que pueden hacer esto, pero, hay un requisito extra: el par de llaves tienen que ser del tipo correspondiente a `Ethereum`: [`ECDSA`](https://www.reddit.com/r/ethereum/comments/81e7f9/what_is_the_encryption_algorithm_used_by_ethereum/).

Las librerías con las que estuve jugando son:

- [`eccrypto`](https://github.com/bitchan/eccrypto)
- [`eth-crypto`](https://github.com/pubkey/eth-crypto)
- [`crypto`](https://nodejs.org/api/crypto.html)

Por ahora tengo una implementación funcional que usa `eth-crypto` PERO (gran pero), solo puede encriptar/decriptar mensajes de menos de 16 letras :(
Le dejé un [`issue`](https://github.com/pubkey/eth-crypto/issues/47) acerca de esto y no me han respondido (capaz nunca lo hagan), así que sigo aprendiendo para ver como resolver esto de manera genérica.

Ya iré avisando.

Saludos,<br />
Gorka
