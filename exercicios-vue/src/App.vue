<script setup>
  import { ref } from 'vue'
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

  const usuarios = ref([
    {nome: 'Bruno', email: 'bruno@gmail.com', telefone: '00000000', idade: '18'},
  ])

  const adicionarUsuario = (novoUsuario) => {
    usuarios.value.push(novoUsuario)
  }
</script>

<template>
  <MeuCabecalho logo="https://vuejs.org/images/logo.png" :secoes="[ 'sobre nós', 'home', 'contato' ]"/>
  <main>
    <MeuTitulo titulo="CONHEÇA O VUE" />
    <MinhaImagem imagem="https://vuejs.org/images/logo.png" descricao="Logo do Vue.js"/>
  </main>
  <MeuParagrafo paragrafo="O vue é um framework para javascript focado na modularização de projetos, criando uma estrutura de componentes
  combinaveis mais faceis de alterar individualmento e compor no seu site, assim, facilitando a criação de layouts unicos e distintos"/>
  <div id="container" style="display: flex; justify-content: space-around; margin: 20px;">
    <div style="display: flex; flex-direction: column; justify-content: center; align-items: center; width: 15%;">
      <MeuParagrafo paragrafo="Além de estilizar, o vue tambêm conta com recursos para interatividade e responsividade do site" />
      <MinhaLista :itens="[ 'Maça', 'Banana', 'Pera' ]" />
    </div>
    <div style="display: flex; flex-direction: column; justify-content: center; align-items: center; gap: 20px; width: 50%;">
      <MeuFormulario @adicionar-usuario="adicionarUsuario"/>
      <MinhaTabela :usuarios="usuarios" />
    </div>
  </div>
</template>

<style scoped>
</style>