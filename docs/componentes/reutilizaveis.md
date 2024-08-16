# Componentes Reutilizáveis no VueJS

Um dos grandes benefícios do VueJS é a facilidade de criar componentes reutilizáveis. Esses componentes podem ser usados em várias partes da aplicação sem a necessidade de duplicar código.

## Exemplo de Componente Reutilizável

```javascript
Vue.component("botao-personalizado", {
  props: ["label"],
  template: "<button>{{ label }}</button>",
});
```

Aqui, o componente `botao-personalizado` pode ser reutilizado em qualquer lugar da aplicação onde um botão com um rótulo personalizado é necessário.

## Ciclo de Vida dos Componentes

O VueJS fornece uma série de "hooks" que permitem a execução de código em diferentes momentos do ciclo de vida de um componente, como:

- **created:** Executado após a criação da instância do componente.
- **mounted:** Executado quando o componente é montado no DOM.
- **updated:** Executado após o componente ser atualizado.
- **destroyed:** Executado quando o componente é destruído.

Esses hooks são úteis para realizar tarefas como requisições de dados ou limpar recursos antes que o componente seja removido.

## Conclusão

Os componentes são uma peça central no VueJS, promovendo a modularização do código e a reutilização de funcionalidades. Com o suporte a propriedades, eventos e ciclo de vida, eles oferecem uma solução poderosa para a criação de interfaces de usuário dinâmicas e escaláveis.
