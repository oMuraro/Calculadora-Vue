<template>
    <section class="acoes">
    <button @click = "($e) => $emit('soma')">+</button>
    <button @click = "($e) => $emit('subtrair')">-</button>
    <button @click = "($e) => $emit('multiplicar')">*</button>
    <button @click = "($e) => $emit('dividir')">/</button>
    <button @click = "($e) => $emit('result')">=</button>
    <button @click = "($e) => $emit('clear')"> C </button>
    </section>
</template>

<style scoped>
    .acoes {
            background-color: cadetblue;
            padding: 10px;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            
        }

        .acoes button {
            width: 50px;
            height: 50px;
            border: 1px solid #616161;
            font-size: 26px;
            margin: 10px;
        }

        button:hover {
            background-color: #616260;
        }
</style>