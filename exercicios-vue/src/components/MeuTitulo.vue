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
        font-family: Arial, Helvetica, sans-serif;
        color: #42b983;
        font-size: 70px;
        padding: 3%;
    }
</style>