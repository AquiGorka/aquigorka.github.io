---
id: 20180527
title: "Static apps y Google Cloud mas gsutil"
date: 2018-05-27T11:27:07+00:00
author: Gorka
layout: post
permalink: /2018/05/static-apps-y-google-cloud-mas-gsutil/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2018/05/google-cloud.png" alt="Google Cloud" />

Hay muchas herramientas que se pueden usar para hacer `deploy` de aplicaciones del tipo front-end o estáticas. Las que yo conocía:

- [surge](http://surge.sh/)
- [dpl](https://github.com/travis-ci/dpl)

… y el muy conocido y tradicional, copiar y pegar usando `ftp` o alguna web console.

La última que empecé a usar es `gsutil` que es parte de las herramientas de cloud de Google (y de `gloud`).

My cómodo, similar a `surge`, el usuario hace login local y de ahí define los commandos que se van a ejecutar.

Para hacer deploy en mi caso fue `rsync`:

```sh
gsutil -m rsync -d -r ./PATH_TO_FOLDER gs://BUCKET_NAME
```

Boom. Listo. Archivos en el bucket. No olvidar hacer que los archivos sean públicos con `gsutil -m acl -r set public-read gs://BUCKET_NAME` y todo en orden.

Así de fácil.

Cómo se instala: https://cloud.google.com/storage/docs/gsutil_install

Los pasos son instalar `gscloud`, inicializarlo (`gscloud init`) y luego preparar la config del bucket (la herramienta lo preguntará directamente).

Rápido y práctico.

Saludos,<br />
Gorka
