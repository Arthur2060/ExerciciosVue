<script setup>
    defineProps({
        itens: Array
    })
</script>

<template>
    <ul>
        <li v-for="item in itens">{{ item }}</li>
    </ul>
</template>

<style scoped>
    ul {
        border-radius: 20px;
        font-family: Arial, Helvetica, sans-serif;
        color: #42b983;
        background-color: rgb(80, 76, 76);
        border: solid 5px gray;
        width: fit-content;
        padding: 3%;
        list-style: none;
    }
    
    li:hover::before {
        content: "• ";
        color: #42b983;
        font-weight: bold;
    }
</style>