<script setup>
    defineProps({
        menssagem: String,
        link: URL
    })
</script>

<template>
    <a :href=link :target="_blank">{{ menssagem }}</a>
</template>

<style scoped>
    a {
        color: #42b983;
    }
</style>