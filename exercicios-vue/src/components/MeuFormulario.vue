<script setup>
    import { ref } from 'vue'

    defineProps({
    })

    const nome = ref('')
    const email = ref('')
    const telefone = ref('')
    const idade = ref('')

    const emit = defineEmits(['adicionar-usuario'])

    function enviar() {
        emit('adicionar-usuario', {
            nome: nome.value,
            email: email.value,
            telefone: telefone.value,
            idade: idade.value,
        })
        nome.value = ''
        email.value = ''
        telefone.value = ''
        idade.value = ''
    }
</script>

<template>
    <form @submit.prevent="enviar">
        <h3>Adicione um usuario na tabela</h3>
        <div class="campo" id="campo-nome">
            <label for="Nome">Nome: </label>
            <input v-model="nome" type="text" id="Nome" name="Nome"/>
        </div>
        <div class="campo" id="campo-email">
            <label for="E-mail">E-mail: </label>
            <input v-model="email" type="email" id="E-mail" name="E-mail"/>
        </div>
        <div class="campo" id="campo-telefone">
            <label for="Telefone">Telefone: </label>
            <input v-model="telefone" type="tel" id="Telefone" name="Telefone"/>
        </div>
        <div class="campo" id="campo-idade">
            <label for="Idade">Idade: </label>
            <input v-model="idade" type="number" id="Idade" name="Idade"/>
        </div>

        <div id="campo-acao" class="campo">
            <button type="submit">Enviar</button>
        </div>
    </form>
</template>

<style scoped>
    form {
        border-radius: 20px;
        font-family: Arial, Helvetica, sans-serif;
        color: #42b983;
        background-color: rgb(80, 76, 76);
        border: solid 5px gray;
        width: fit-content;
        padding: 1% 3%;
    }

    .campo {
        margin-bottom: 10px;
    }

    label {
        display: block;
        margin-bottom: 5px;
    }

    input {
        width: 100%;
        padding: 8px;
        box-sizing: border-box;
        border-radius: 5px;
        border-color: gray;
        background-color: transparent;
        color: #42b983;
    }

    #campo-acao {
        text-align: center;
        margin-top: 15px;
    }

    #campo-acao > button {
        background-color: #42b983;
        color: black;
        padding: 10%;
        border: none;
        border-radius: 20px;
        font-weight: bold;
        font-size: 22px;
    }
</style>