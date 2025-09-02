<script setup>
    defineProps({
        items: Array
    })
</script>

<template>
    <form>
        <div class="campo" v-for="(item, index) in items" :key="index">
            <label :for="item">{{ item }}</label>
            <input type="text" :id="item" :name="item" />
        </div>

        <div id="acao">
            <button type="submit">Enviar</button>
        </div>
    </form>
</template>

<style scoped>
    form {
        border-radius: 20px;
        font-family: Arial, Helvetica, sans-serif;
        color: #42b983;
        background-color: rgb(80, 76, 76);
        border: solid 5px gray;
        width: fit-content;
        padding: 3%;
    }

    .campo {
        margin-bottom: 10px;
    }

    label {
        display: block;
        margin-bottom: 5px;
    }

    input {
        width: 100%;
        padding: 8px;
        box-sizing: border-box;
        border-radius: 5px;
        border: 1px solid #ccc;
    }

    #acao {
        text-align: center;
        margin-top: 15px;
    }
</style>