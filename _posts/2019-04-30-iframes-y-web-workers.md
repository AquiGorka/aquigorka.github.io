---
id: 20190430
title: iframes y Web Workers
date: 2019-04-30T21:03:07+00:00
author: Gorka
layout: post
permalink: /2019/04/iframes-y-web-workers/
categories:
  - Ideas
---

<img style="margin: auto;" src="/public/img/2019/04/sandbox.png" alt="Sandbox" />

Resulta que por cuestiones de trabajo me vengo a enterar que los [`Web Workers`](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers) tienen acceso a los recursos de `localStorage` cuando no se les ejecuta con un origen opaco (`opaque origin` - [referencia](https://html.spec.whatwg.org/multipage/workers.html#dom-worker)).

La propuesta sería entonces restringir ese origen para poder limitar el acceso, pero cuando el `Web Worker` va a recibir un script grande (más de 2 megas grande), esto se nota - osea, tarda la ejecución y pues no es la mejor experiencia para el usuario.

Se vieron e intentaron varias propuestas ([`acá están`](https://github.com/aragon/aragon/pull/808) si a alguien le intersan) pero ninguna fue final. Tirando ideas llegó otra que proponía usar los `Web Workers` dentro de un `iframe` limitado por `sandbox` ([`sanboxed iframes`](https://www.html5rocks.com/en/tutorials/security/sandboxed-iframes/)), así que me puse a _hackear_ para ver si lo podía hacer funcionar.

El tema es que el código que se va a ejectuar en el `Web Worker` es "dinámico", osea, no le vamos simplemente dar una `URL` donde está el script que va a ejecutar, sino que hay que darle un [`Blob`](https://developer.mozilla.org/en-US/docs/Web/API/Blob), por lo cual va a haber problemas. Resumiendo:

- el iframe va a tener `sandbox` y sólo e le va a dar el permiso de `allow-scripts`
- hay que usar `JavaScript` para generar el código que se va a ejecutar en el `iframe`
- el `Web Woker` va a mandar mensajes al `iframe` y el mismo los tiene que responder al contexto que lo ejecutó

Solución propuesta:

```JavaScript
class IframeWorker extends EventTarget {
  constructor(scriptUrl, id) {
    super()
    this.id = id
    this.iframe = document.createElement('iframe')
    this.iframe.sandbox = 'allow-scripts'

    const source = `
      <script>
        const init = async () => {
          const res = await fetch(url, { mode: 'cors' })
          const blob = await res.blob()
          const workerURL = URL.createObjectURL(blob)
          const worker = new Worker(workerUrl, { name: '${id}' })
          worker.addEventListener('error', error => window.parent.postMessage({ from: '${id}', error }, '*'), false)
          worker.addEventListener('message', event => window.parent.postMessage({ from: '${id}', msg: event.data }, '*'), false)
          window.addEventListener('message', ({ data }) => worker.postMessage(data))
          URL.revokeObjectURL(workerUrl)
        }
        init()
      </script>
    `
    this.iframe.srcdoc = source
    document.body.appendChild(this.iframe)
    window.addEventListener('message', this.handleIframeMessage, false)
  }

  postMessage(msg) {
    this.iframe.contentWindow.postMessage(msg, '*')
  }

  destroy() {
    window.removeListener('message', this.handleIframeMessage)
    document.removeChild(this.iframe)
    this.iframe = null
  }

  handleIframeMessage = ({ source, data: { from, error, msg } }) => {
    if (source === this.iframe.contentWindow && from === this.id) {
      this.dispatchEvent(
        new MessageEvent(error ? 'error' : 'message', {
          data: error || msg,
        })
      )
    }
  }
}

export default iframeWorker
```

Lo que se hizo cumple con lo que queríamos:

1. Inyectar el código directamente en la clase, para lo cual se recivbe `scriptUrl`, que se transforma en un `blob`, así se puede usar directamente en el `Worker` en el `iframe`.
1. Para que el `iframe` ejecute el código inyectado hay que _settear_ la propiedad `srcdoc` en lugar de `src` o de modificar el cuerpo dinámicamente (esos métodos tirarían `DOM Exception` por que el `iframe` está en un `sandbox`).
1. Simular la interfaz de un `Worker` para hacer comunicación transparente, en este caso está el método `postMessage` y la emisión de eventos del tipo `MessageEvent`
1. Nota la implementación del método `handleIframeMessage` necesita de un transpilador para mantener contexto, de lo contrario tendría que hacerse un `bind` en el constructor (`this.handleIframeMessage = this.handleIframeMessage.bind(this)`)

Y así quedó [la fiesta](https://github.com/aragon/aragon/pull/819).

Bueno, con esta clase se pueden tener `Worker`s ejectuandose un contexto `JS` sin que tengan acceso a los `store`s de `IndexedDB` del mismo. No es algo normal pero es algo que le va a venir bien a quien lo esté buscando.

Saludos,<br />
Gorka
