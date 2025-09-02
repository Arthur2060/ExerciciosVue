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
        padding: 10px 20px;
        background-color: rgb(80, 76, 76);
        color: #42b983;
        width: 100%;
        height: fit-content;
    }

    img {
        height: 40px;
    }

    nav ul {
        list-style: none;
        display: flex;
        gap: 15px;
        margin: 0;
        padding: 0;
    }

    nav li {
        cursor: pointer;
    }

    nav li:hover {
        text-decoration: underline;
    }
</style>