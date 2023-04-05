<template>
    <section class="botoes">
        <button @click="($e) => $emit('digitar', 1)"> 1</button>
        <button @click="($e) => $emit('digitar', 2)"> 2</button>
        <button @click="($e) => $emit('digitar', 3)"> 3</button>
        <button @click="($e) => $emit('digitar', 4)"> 4</button>
        <button @click="($e) => $emit('digitar', 5)"> 5</button>
        <button @click="($e) => $emit('digitar', 6)"> 6</button>
        <button @click="($e) => $emit('digitar', 7)"> 7</button>
        <button @click="($e) => $emit('digitar', 8)"> 8</button>
        <button @click="($e) => $emit('digitar', 9)"> 9</button>
        <button @click="($e) => $emit('digitar', 0)"> 0</button>
        </section>
</template>

<style scoped>
    .botoes {
            display: flex;
            flex-wrap: wrap;
            margin-top: 5px;
            border: 1px solid #616161;
            background-color: red;
            padding: 10px;
            justify-content: center;
        }

        .botoes button{
            margin-top: 50px;
            border: 50px;
            border: 1px solid #616161;
            background: white;
            font-size: 26px;
            width: 50px;
            height: 50px;
            margin: 10px;
        }

        button:hover {
            background-color: #616260;
        }
</style>