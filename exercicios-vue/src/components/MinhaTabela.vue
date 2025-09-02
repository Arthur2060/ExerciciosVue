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
</style>