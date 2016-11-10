# Como converter uma imagem PSD para SVG

**Autor:** Augusto TMW

---

### No photoshop:

1. Clique com o botão direito na camada da imagem e converta-a em um "Smart Object";
2. Clique com o botão direito na camada novamente e clique em "Export Contents..."
3. Salve o arquivo _**.psb**_ ou _**.ai**_ e abra o Ilustrator.

### No Ilustrator

1. Abra o arquivo _**.psb**_ ou _**.ai**_ salvo nos passos anteriores;
2. Clique no menu _**Select > All**_;
3. Clique no menu _**File > Save as...**_;
4. Selecione no combobox _**"Formato"**_ o formato _**SVG**_ e salve o arquivo _**.svg**_;


### Num editor de texto

1. Abra o arquivo _**.svg**_;
2. Remova as tags desnecessárias:
    ```html
    tag xml
    <?xml version="1.0" encoding="utf-8"?>

    comentários
    <!-- Generator: Adobe Illustrator 16.0.0, SVG Export Plug-In . SVG Version: 6.00 Build 0)  -->

    doctype
    <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

    group tags
    <g id="Shape_1">
        <g>
        </g>
    </g>

    etc.

    ```
3. Abra o [icomoon](https://icomoon.io/app) ou qualquer outro gerador de fonte de sua preferência e importe a fonte à fins de teste.


### Vídeos referência
* (https://www.youtube.com/watch?v=znZlmDYOPaA)
* (https://www.youtube.com/watch?v=YqdQrTPsUeE)