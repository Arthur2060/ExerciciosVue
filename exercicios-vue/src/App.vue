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
    <MeuTitulo titulo="CONHEÇA O VUE" />
    <MinhaImagem imagem="https://vuejs.org/images/logo.png" descricao="Logo do Vue.js"/>
  </main>
  <MeuParagrafo paragrafo="O vue é um framework para javascript focado na modularização de projetos, criando uma estrutura de componentes
  combinaveis mais faceis de alterar individualmento e compor no seu site, assim, facilitando a criação de layouts unicos e distintos"/>
  <div style="display: flex; margin: 2%; align-items: center;">
    <MinhaLista :itens="[ 'Maça', 'Banana', 'Pera' ]" />
    <MeuParagrafo paragrafo="Além de estilizar, o vue tambêm conta com recursos para interatividade e responsividade do site" />
  </div>
</template>

<style scoped>
</style>