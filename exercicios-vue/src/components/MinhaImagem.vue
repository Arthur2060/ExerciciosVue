<script setup>
    defineProps({
        imagem: Image,
        descricao: String
    })
</script>

<template>
    <img :src=imagem :alt=descricao />
</template>

<style scoped>
</style>