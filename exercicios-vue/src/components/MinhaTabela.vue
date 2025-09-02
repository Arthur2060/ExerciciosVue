<script setup>
    defineProps({
        usuarios: Array
    })
</script>

<template>
    <table>
        <thead>
            <tr>
                <td><strong>Nome</strong></td>
                <td><strong>Idade</strong></td>
                <td><strong>E-mail</strong></td>
                <td><strong>Telefone</strong></td>
            </tr>
        </thead>
        <tr v-for="(usuario, index) in usuarios" :key="index">
            <td>{{ usuario.nome }}</td>
            <td>{{ usuario.idade }}</td>
            <td>{{ usuario.email }}</td>
            <td>{{ usuario.telefone }}</td>
        </tr>
    </table>
</template>

<style scoped>
    table {
        border-radius: 20px;
        font-family: Arial, Helvetica, sans-serif;
        color: #42b983;
        background-color: rgb(80, 76, 76);
        border: solid 5px gray;
        width: fit-content;
        padding: 3%;
        text-align: left;
        border-collapse: collapse;
    }

    td {
        padding: 8px 12px;
    }

    thead {
        border-bottom: solid 3px gray;
    }
</style>