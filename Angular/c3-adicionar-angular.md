# Como adicionar o c3.js no Angular

1. Instale o c3 via terminal na raíz do projeto:

```terminal
npm install c3
npm install @types/c3
```
2. Adicione `../node_modules/c3/c3.min.css`, ao arquivo _**.angular-cli.json** => style section_

```json
angular-cli.json

{
  ...
  "projects": {
    "Chart": {
      ...
      "architect": {
        "build": {
          ...
          "options": {
            ...
            "styles": [
              "node_modules/c3/c3.min.css",
              "src/styles.css"
            ]
            ...
          },
          ...
        },
        ...
        "test": {
          ...
          "options": {
            ...
            "styles": [
              "node_modules/c3/c3.min.css",
              "src/styles.css"
            ],
            ...
          }
        },
        ...
      }
    },
    ...
  },
  ...
}

```

3. Adicione  `<div id="chart"></div>` ao template do seu componente;

4. Adicione `import * as c3 from 'c3';` ao seu componente;

5. Adicione os códigos [relativos ao seu gráfico](https://c3js.org/examples.html) no seu typescript assim:

```typescript
ngAfterViewInit() {
    let chart = c3.generate({
    bindto: '#chart',
        data: {
            columns: [
                ['data1', 30, 200, 100, 400, 150, 250],
                ['data2', 50, 20, 10, 40, 15, 25]
            ]
        }
    });
}
```

- Referência: [How add C3 charts to angular 2+ project](https://stackoverflow.com/questions/46250941/how-add-c3-charts-to-angular-2-project)