<script setup>
    defineProps({
        logo: Image,
        secoes: Array
    })
</script>

<template>
    <header>
        <img :src=logo alt="Logo" />
        <nav>
            <ul>
                <li v-for="secao in secoes">{{ secao }}</li>
            </ul>
        </nav>
    </header>
</template>

<style scoped>
    header {
        display: flex;
        justify-content: space-around;
        align-items: center;
        background-color: rgb(80, 76, 76);
        color: #42b983;
        width: 100%;
        height: 5vh;
        border-bottom: solid 2px gray;
    }

    img {
        height: 40px;
    }

    nav ul {
        list-style: none;
        display: flex;
        margin: 0;
        padding: 0;
    }

    nav li {
        display: flex;
        align-items: center;
        transition: all 0.3s;
        height: 5vh;
        padding: 2%;
    }

    nav li:hover {
        background-color: gray;
    }
</style>