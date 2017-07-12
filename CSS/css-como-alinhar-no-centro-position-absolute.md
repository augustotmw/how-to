# Como alinhar um elemento de posição absoluta no centro?

**Autor:** Augusto TMW

1. Técnica 1:

```css

div {
    position: absolute;
    margin: auto;
    left: 0;
    right: 0;
}

```


2. Técnica 2:

```css

div {
    position: absolute;
    left: 50%;
    top: 50%;
    margin: auto;
    -webkit-transform: translateX(-50%);
    -moz-transform: translateX(-50%);
    -ms-transform: translateX(-50%);
    -o-transform: translateX(-50%);
    transform: translateX(-50%);
}

div.centro-vertical {
    top: 50%;
    -webkit-transform: translate(-50%,-50%);
    -moz-transform: translate(-50%,-50%);
    -ms-transform: translate(-50%,-50%);
    -o-transform: translate(-50%,-50%);
    transform: translate(-50%,-50%);    
}

```

#### Navegadores observados:

* Google Chrome
* Safari
* Firefox
* Opera