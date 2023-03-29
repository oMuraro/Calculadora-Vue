<template>
    <section class="resultado">
        {{  valor }}
    </section>
</template>

<script>
    export default  {
        props: {
            valor: {
                required: true
            }
        }
    }
</script>

<style scoped>
.resultado {
    width: 300px;
    height: 100px;
    border: 1px solid #616161;
    background-color: white;
    font-size: 50px;
    display: flex;
    justify-content: end;
    align-items: center;
}
</style>