# Ionic

## SplashScreen

- versão testada: 3


## Para evitar que apareça:

##### no arquivo `config.xml`, troque na tag `<preference>` de `name="SplashScreen"` o valor `"none"`:

```xml
<preference name="SplashScreen" value="none"/>
```


## Para evitar que oculte automático:

##### no arquivo `config.xml`, adicione as seguintes tags `<preference>`:

```xml
<preference name="FadeSplashScreen" value="false" />
<preference name="AutoHideSplashScreen" value="false" />
```


