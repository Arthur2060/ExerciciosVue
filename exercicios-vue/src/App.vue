<script setup>
  import MeuTitulo from './components/MeuTitulo.vue'
  import MeuParagrafo from './components/MeuParagrafo.vue'
  import MinhaLista from './components/MinhaLista.vue'
  import MinhaImagem from './components/MinhaImagem.vue'
  import MeuLink from './components/MeuLink.vue'
  import MinhaTabela from './components/MinhaTabela.vue'
  import MeuCard from './components/MeuCard.vue'
  import MeuRodape from './components/MeuRodape.vue'
  import MeuCabecalho from './components/MeuCabecalho.vue'
  import MeuFormulario from './components/MeuFormulario.vue'
</script>

<template>
  <MeuCabecalho logo="https://vuejs.org/images/logo.png" :secoes="[ 'sobre nós', 'home', 'contato' ]"/>
  <main>
    <MinhaImagem imagem="https://vuejs.org/images/logo.png" descricao="Logo do Vue.js"/>
  </main>
</template>

<style scoped>
</style>