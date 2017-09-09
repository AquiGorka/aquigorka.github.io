---
id: 20170909
title: "Buenas prácticas para pasar contraseñas"
date: 2017-09-09T11:27:07+00:00
author: Gorka
layout: post
permalink: /2017/09/buenas-practicas-para-pasar-contrasenas/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2017/09/cipher_disk.jpg" alt="Cipher Disk" />

> Only the paranoid will survive and inherit the earth

## openssl

Hablemos primero de lo que pasó: necesité que me mandaran una contraseña, la manera "insegura" (y que creo todos hemos tipicamente usado) es pasarla por email o chat (a veces en partes para hacerlo más seguro, a veces no).

Y, para que me llegara una contraseña me encontré decifrando direcciones url + decriptando hashes + borrando todo y guardando las cosas en una "caja segura".

La idea es que, para pasar una contraseña la buena práctica implica usar **por lo menos** dos cananales diferentes para transmitir datos - así si alguien está escuchando un canal, sólo escucha parte de la conversación.

Lo divertido es que a través de uno de los canales se hace llegar una contraseña encriptada y a través del otro, la clave para decriptar la contraseña original. Fue ahí donde descubrí **openssl**.

Con esta herramienta puedo encriptar/decriptar (cifrar/descifrar) palabras o frases y así transmitirlas - de una manera en la que para "entenderlas" se necesita la clave descifradora.

### ¿Cómo funciona?

```
echo 'Esta sería la contraseña' | openssl enc -base64 -e -aes-256-cbc -pass pass:esta_es_la_clave_cifradora_descifradora
```

Y esto nos da: `U2FsdGVkX1/l9mGydcS6YSQHL7Mp564njMvaBpJZnEv/IR3mfg2Ojh3NMF/2GYEr`

Genial, y luego? Pues luego la podemos descifrar así:

```
echo U2FsdGVkX1/l9mGydcS6YSQHL7Mp564njMvaBpJZnEv/IR3mfg2Ojh3NMF/2GYEr | openssl enc -aes-256-cbc -d -a
```

Y ahí nos pregunta por la clave (también se le podríamos dar como argumento en la forma `-pass pass:esta_es_la_clave_cifradora_descifradora`).

Y **kapow!**: `Esta sería la contraseña`


### También sirve para archivos

- Cifrar

```
openssl aes-256-cbc -a -salt -in 'ruta_y_nombre_al_archivo_a_encriptar' -out 'ruta_y_nombre_al_archivo_encriptado' -pass pass:esta_seria_la_clave
```

- Descifrar

```
openssl aes-256-cbc -d -a -in 'ruta_y_nombre_al_archivo_encriptado' -out 'ruta_y_nombre_al_archivo_desencriptado'
```

Así que bueno, aprendiendo de buenas prácticas y nuevas herramientas.

Saludos,
Gorka

PD - la imagen es de un tipo de cifrado conocido como [Caesar Cipher](https://en.wikipedia.org/wiki/Caesar_cipher)

PD2 - buscando imágenes de `cipher disk` para este post como que me parace que el zodiaco, calendario azteca y las monedas se parecen mucho a este tipo de discos - paranoia lo mío?
