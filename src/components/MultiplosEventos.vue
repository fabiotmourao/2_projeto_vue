<template>
    <div>
        <button @click="primeiro(primeiroTxt, $event), segundo(segundoTxt, $event), terceiro(terceiroTxt, $event)">Ativar múltiplos eventos</button>
        <p> {{ multiplos_eventos }} </p>
    </div>
</template>

<script>
export default {
    name: "MultiplosEventos",
    data() {
        return {
            multiplos_eventos: "",
            primeiroTxt: "primeiro evento sendo executado!",
            segundoTxt: "segundo evento sendo executado!"
        }
    },
    methods: {
        primeiro(primeiro, e){
            this.multiplos_eventos = primeiro;
        },
        segundo(segundoTxt, e){
           setTimeout(() => this.multiplos_eventos = segundoTxt, 800);
        },
        terceiro(terceiroTxt, e){
           setTimeout(() => this.multiplos_eventos = " ", 1500);
        }
    }
}
</script>
<style scoped>
    div {
        margin: 10rem;
    }
</style>