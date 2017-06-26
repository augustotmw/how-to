# Como fazer um link triangular?

**Autor:** Augusto TMW

1. Crie um elemento que irá conter o link, como por exemplo, uma *"div"*:

```html
<div>
    <a href="#"></a>
</div>
```

2. No elemento pai, adicione os seguintes estilos:

```css
div {
    position:relative;
    overflow:hidden;

    /* opcionais: */
    width: 100%;
    height: 100%;
    border: 3px solid red;
}
```

3. No link, adicione os seguintes estilos:

```css
a{
    position:absolute;
    -webkit-transform-origin: 100% 0;
    -moz-transform-origin: 100% 0;
    -ms-transform-origin: 100% 0;
    -o-transform-origin: 100% 0;
    transform-origin: 100% 0;
    -webkit-transform: rotate(-45deg);
    -moz-transform: rotate(-45deg);
    -ms-transform: rotate(-45deg);
    -o-transform: rotate(-45deg);
    transform: rotate(-45deg);

    /* opcionais: */
    width: 40px;
    height: 40px;
    top: -36px;
    right: 7px;
    background: blue;

}
```

### Referências:

* (https://stackoverflow.com/questions/25917610/triangular-link-area)