<template>
    <p v-if="estado_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidade!</p>
    <p>Utilizo as seguintes tecnlogias:</p>
    <ul>
        <li>PHP / Laravel</li>
        <li>Mysql</li>
        <li>Iniciando com vueJS</li>
    </ul>
    <div>
        <button @click="showEmail">
            {{ textButton }}        
        </button>
    </div>
    <p v-show="exibir">Mande uma mensagem para: {{ email}}</p>
    <p> Para acessar meu portifólio <a v-bind:href="link" target="_blank" >Clique aqui</a></p>
    <Picture />
</template>

<script>
import Picture from './Picture.vue'

export default {
    name: "Info",
    components: {
        Picture,
    },
    data() {
        return{
            estado_trabalhando: true,
            exibir: false,
            email: 'fabio@email.com',
            link: 'https://google.com',
            textButton: 'Exibir E-mail'
        }
    },
    methods:{
        showEmail(){
            this.exibir = !this.exibir
            if(!this.exibir){
                this.textButton = 'Exibir E-mail'
            } else {
                this.textButton = 'Ocultar E-mail'
            }
        }
    }
}
</script>