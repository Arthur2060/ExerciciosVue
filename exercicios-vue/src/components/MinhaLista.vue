<script setup>
    import { ref } from 'vue';

    const props = defineProps({
        itens: Array
    })

    const lista = ref([...props.itens])
    const novoItem = ref('')

    function adicionarItem() {
        if (novoItem.value.trim()) {
            lista.value.push(novoItem.value)
            novoItem.value = ''
        }
    }
</script>

<template>
    <div id="container">
        <h5>Escreva algo para adicionar</h5>
        <div id="container-adicao">
            <input v-model="novoItem" type="text" id="textoNovoItem"><button @click="adicionarItem" id="botaoAdicionar">Adicionar</button>
        </div>
        <ul id="lista">
            <li v-for="item in lista" :key="item" class="item">{{ item }}</li>
        </ul>
    </div>
</template>

<style scoped>
    #container {
        border-radius: 20px;
        font-family: Arial, Helvetica, sans-serif;
        color: #42b983;
        background-color: rgb(80, 76, 76);
        border: solid 5px gray;
        width: fit-content;
        padding: 10%;
        margin: 3%;
    }

    ul {
        list-style: none;
    }
    
    #container-adicao {
        display: flex;
        gap: 3px;
    }

    #textoNovoItem {
        background-color: transparent;
        color: #42b983;
        border-color: gray;
        border-radius: 5px;
    }

    #botaoAdicionar {
        background-color: #42b983;
        color: black;
        border: none;
        border-radius: 20px;
        padding: 2%;
    }

    li:hover::before {
        content: "•";
        color: #42b983;
        font-weight: bold;
    }
</style>