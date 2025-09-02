<script setup>
    defineProps({
        titulo: String
    })
</script>

<template>
    <h1>{{ titulo }}</h1>
</template>

<style scoped>
    h1 {
        border-radius: 20px;
        font-family: Arial, Helvetica, sans-serif;
        color: #42b983;
        background-color: rgb(80, 76, 76);
        border: solid 5px gray;
        width: fit-content;
        padding: 3%;
    }
</style>