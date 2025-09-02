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
        border-radius: 20px;
        font-family: Arial, Helvetica, sans-serif;
        color: #42b983;
        background-color: rgb(80, 76, 76);
        border: solid 5px gray;
        width: fit-content;
        padding: 3%;
    }
</style>