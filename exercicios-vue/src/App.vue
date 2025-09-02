<script setup>
  import MeuTitulo from './components/MeuTitulo.vue'
  import MeuParagrafo from './components/MeuParagrafo.vue'
  import MinhaLista from './components/MinhaLista.vue'
  import MinhaImagem from './components/MinhaImagem.vue'
  import MeuLink from './components/MeuLink.vue'
  import MinhaTabela from './components/MinhaTabela.vue'
  import MeuCard from './components/MeuCard.vue'
</script>

<template>
  <MeuTitulo titulo="Aprendendo Vue.js"/>
  <MeuParagrafo paragrafo="Este é um parágrafo de exemplo para demonstrar a passagem de props em Vue.js."/>
  <MinhaLista :itens="['Item 1', 'Item 2', 'Item 3', 'Item 4']"/>
  <MinhaImagem imagem="https://vuejs.org/images/logo.png" descricao="Logo do Vue.js"/>
  <MeuLink url="https://vuejs.org" texto="Visite o site oficial do Vue.js"/>
  <MinhaTabela :usuarios="[
    { nome: 'Alice', idade: 30, email: 'alice@gmail.com', telefone: '000000000' },
    { nome: 'Bob', idade: 25, email: 'bob@gmail.com', telefone: '000000000' },
    { nome: 'Charlie', idade: 35, email: 'charlie@gmail.com', telefone: '000000000' }
  ]"/>
  <MeuCard titulo="Card de Exemplo" paragrafo="Este é um card que utiliza props para exibir um título e um parágrafo."/>
</template>

<style scoped>
</style>