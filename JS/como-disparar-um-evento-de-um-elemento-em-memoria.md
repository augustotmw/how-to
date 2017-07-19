# JS - Como disparar um evento a partir de um elemento em memória?

**Autor:** Augusto TMW

* P.e., crie um link:

```javascript
var a = window.document.createElement("a");
a.target = '_blank';
a.href = url;

```

* Crie uma instância de eventos de mouse e configure o início do clique:

```javascript
var e = window.document.createEvent("MouseEvents");
    e.initMouseEvent("click", true, true, window, 0, 0, 0, 0, 0, false, false, false, false, 0, null);
```

* Dispare o evento em relação ao elemento:

```javascript
    a.dispatchEvent(e);
```


##### Sintaxe:

_object.**initMouseEvent**(eventName, bubbles, cancelable, view, detail, screenX, screenY, clientX, clientY, ctrlKey, altKey, shiftKey, metaKey, button, relatedTarget);_
