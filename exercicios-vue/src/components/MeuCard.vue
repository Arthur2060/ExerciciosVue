<script setup>
    defineProps({
        titulo: String,
        paragrafo: String
    })
</script>

<template>
    <div class="card">
        <h3>{{ titulo }}</h3>
        <p>{{ paragrafo }}</p>
    </div>
</template>

<style scoped>
    .card {
        border-radius: 20px;
        font-family: Arial, Helvetica, sans-serif;
        color: #42b983;
        background-color: rgb(80, 76, 76);
        border: solid 5px gray;
        width: 10vw;
        padding: 1%;
        margin: 10px;
    }
</style>