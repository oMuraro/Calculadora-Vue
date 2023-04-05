<template>
    <form @submit.prevent="$e => salvarAluno()">
        <input type="text" placeholder="Nome" v-model="nome" id="inputNome">
        <input type="number" placeholder="Idade" v-model="idade" id="inputIdade">
        <input type="text" placeholder="Série" v-model="serie" id="inputSerie">
        <button>Salvar</button>
    </form>
    <hr>
    <ul v-for="aluno, index in this.dados">
        <li> Nome: {{  aluno.nome }} </li>
        <li> Idade: {{  aluno.idade }} </li>
        <li> Série: {{ aluno.serie }} </li>
        <button @click = "$e => deletarAluno(index)"> Deletar </button>
        <button @click = "$e => editarAluno(index)"> Editar </button>
    </ul>
</template>

<script>
    import alunos from "~/alunos.json"

    export default {
        data(){
            return{
                dados: alunos,
                nome: "",
                idade: "",
                serie: ""
            }
        },
        methods: {
            salvarAluno() {
                this.dados.push( { "nome": this.nome, "idade": this.idade, "serie": this.serie });
            },
            deletarAluno(index) {
                this.dados.splice(index, 1)
            },
            editarAluno(index) {
                this.dados[index].nome = prompt ("Altere o Nome", this.dados[index].nome)
                this.dados[index].idade = prompt ("Altere a Idade", this.dados[index].idade)
                this.dados[index].serie = prompt ("Altere a Série", this.dados[index].serie)
            }
        }
    }
</script>

<style scoped>
    * {
        font-size: 1.2em;
    }
</style>