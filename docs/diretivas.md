# Diretivas no VueJS

As diretivas são uma das funcionalidades mais poderosas do VueJS. Elas são utilizadas para manipular o DOM diretamente, adicionando comportamento especial a elementos HTML.

## Diretivas Comuns

- **`v-if`:** Renderiza condicionalmente um bloco de código.
- **`v-for`:** Renderiza um bloco de código várias vezes, baseado em uma lista de dados.
- **`v-bind`:** Vincula atributos a expressões.
- **`v-model`:** Cria uma ligação bidirecional entre um campo de formulário e os dados.
- **`v-show`:** Exibe ou esconde elementos com base em uma condição, sem remover o elemento do DOM.

## Exemplos de Uso

### `v-if`

```html
<div v-if="isVisible">
  Este conteúdo só será exibido se `isVisible` for verdadeiro.
</div>
```

### `v-for`

```html
<ul>
  <li v-for="item in items" :key="item.id">{{ item.name }}</li>
</ul>
```

### `v-bind`

```html
<img v-bind:src="imageUrl" alt="Imagem dinâmica" />
```

### `v-model`

```html
<input v-model="message" placeholder="Digite uma mensagem" />
```

## Criando Diretivas Personalizadas

Além das diretivas embutidas, o VueJS permite a criação de diretivas personalizadas para casos específicos. Diretivas personalizadas são úteis quando você precisa de um comportamento especial em elementos do DOM.

### Exemplo de Diretiva Personalizada

```javascript
Vue.directive("foco", {
  inserted: function (el) {
    el.focus();
  },
});
```

No exemplo acima, a diretiva `foco` automaticamente foca no elemento associado quando ele é inserido no DOM.

### Usando a Diretiva Personalizada

```html
<input v-foco />
```

A diretiva `v-foco` faz com que o campo de entrada receba o foco automaticamente quando renderizado.

## Conclusão

As diretivas no VueJS são uma maneira eficiente de adicionar comportamentos dinâmicos a elementos de interface. Desde diretivas simples embutidas, como `v-if` e `v-for`, até a criação de suas próprias diretivas personalizadas, o VueJS oferece uma flexibilidade impressionante para manipulação do DOM.
