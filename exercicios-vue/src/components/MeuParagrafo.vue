<script setup>
    defineProps({
        paragrafo: String
    })
</script>

<template>
    <p>{{ paragrafo }}</p>
</template>

<style scoped>
    p {
        font-family: Arial, Helvetica, sans-serif;
        color: #42b983;
        background-color: rgb(80, 76, 76);
        width: fit-content;
        height: fit-content;
        padding: 3%;
    }
</style>