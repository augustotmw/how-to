# Como rodar a instância do Ionic com os estilos de uma plataforma específica?


- Abra o arquivo `src/app/app.module.ts`;
- Procure pela chamada `IonicModule.forRoot(MyApp)`;
- Adicione a configuração:

```typescript
IonicModule.forRoot(MyApp, {
    mode: 'ios'
})
```

- Opções:
    -  `ios` : para iOS;
    - `md` : para Android;
    - `wp` : para Windows Phone;
