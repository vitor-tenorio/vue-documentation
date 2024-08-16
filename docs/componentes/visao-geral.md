# Visão Geral dos Componentes no VueJS

Componentes são a base da construção de aplicativos no VueJS. Eles permitem que você divida a interface do usuário em blocos independentes, reutilizáveis e gerenciáveis.

## Criando um Componente

A criação de um componente é feita declarando uma nova instância do Vue com uma propriedade `template` ou utilizando o sistema de Single File Components (SFC).

```javascript
Vue.component("meu-componente", {
  template: "<div>Este é um componente!</div>",
});
```

## Propriedades e Eventos

Propriedades (`props`) permitem a passagem de dados para componentes filhos, enquanto eventos (`$emit`) permitem a comunicação do filho para o pai.
