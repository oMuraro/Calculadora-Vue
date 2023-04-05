<template>
    <main>
        <Display 
            :valor="display"
        />
        <Numbers 
            @digitar="digitar"
        />
        <Actions 
            @soma="soma"
            @result="result"
            @clear="clear"
            @subtrair="subtrair"
            @multiplicar="multiplicar"
            @dividir="dividir"
        />
    </main>
</template>

<script>
import { Result } from 'postcss';

    export default {
        data() {
            return {
                display: "",
                number1: "",
                number2: "",
                operator: ""
            }
        },
        methods: {
            digitar(valor) {
                if (this.operator === "resultado") {
                    this.clear();
                    this.operator = "";
                } 
                this.display += valor;    
            },
            soma() {
                this.number1 = parseInt(this.display);
                this.display = "";
                this.operator = "soma";
            },
            subtrair() {
                this.number1 = parseInt(this.display);
                this.display = "";
                this.operator = "subtrair";
            },
            multiplicar() {
                this.number1 = parseInt(this.display);
                this.display = "";
                this.operator = "multiplicar";
            },
            dividir() {
                this.number1 = parseInt(this.display);
                this.display = "";
                this.operator = "dividir";
            },
            result() {
                if (this.operator === "soma") {
                    this.number2 = parseInt(this.display);
                    this.display = this.number1 + this.number2;
                }
                if (this.operator === "subtrair") {
                    this.number2 = parseInt(this.display);
                    this.display = this.number1 - this.number2;
                }
                if (this.operator === "multiplicar") {
                    this.number2 = parseInt(this.display);
                    this.display = this.number1 * this.number2;
                }
                if (this.operator === "dividir") {
                    this.number2 = parseInt(this.display);
                    this.display = this.number1 / this.number2;
                }
                this.operator = "resultado";
            },
            clear() {
                this.display = "";
                this.number1 = "";
                this.number2 = "";
            }
        }
    }
</script>

<style scoped>
    * { padding: 0; margin: 0};

html {
    height: 100%;
}

body {
    height: 100%;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

main {
    width: 300px;
    background-color: aqua;
    padding: 30px;
}
</style>