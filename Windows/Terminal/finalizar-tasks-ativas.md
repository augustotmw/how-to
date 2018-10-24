# Como finalizar tasks ativas do Windows via terminal?

```
taskkill -f -im <nome do .exe em questao sem extensão>*
```

por exemplo, para finalizar todas as tasks do aplicativo node.exe:

```
taskkill -f -im node*
```