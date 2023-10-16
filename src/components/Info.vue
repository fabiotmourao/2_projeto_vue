<template >
    <p v-if="estado_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidade!</p>
    <p>Utilizo as seguintes tecnlogias back-end:</p>
    <ul>
        <li v-for="(technology, index)  in backend_technologies" :key="index">
            {{ technology }}
        </li>
    </ul>
        <p>Utilizo as seguintes tecnlogias front-end:</p>
    <ul>
        <li v-for="(technology)  in frontend_technologies" :key="technology.id">
            {{ technology.language }}
        </li>
    </ul>
    <div>
        <button @click="showEmail">
            {{ textButton }}        
        </button>
    </div>
    <p v-show="exibir">Mande uma mensagem para: {{ email}}</p>
    <p class="teste"> Para acessar meu portifólio <a v-bind:href="link" target="_blank" >Clique aqui</a></p>
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
            textButton: 'Exibir E-mail',
            backend_technologies:['PHP/Laravel','Mysql','JavaScript'],
            frontend_technologies: [
                {id: 1, language: 'HTML5'},
                {id: 2, language: 'CSS3'},
                {id: 3, language: 'Vue 3'}
            ]
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

<style>
    p {
       padding: 1rem;
    }

    ul {
        list-style: none;
        padding-top: 1rem;
    }
    
    li {
        margin: 1rem;
    }

    button{
        height: 56px;
        border: 0;
        background: #04D361;  
        border-radius: 8px;

        font-family: 'Archivo';
        
        font-weight: 600;
        font-size: 16px;
        line-height: 26px;

        color: #FFFFFF;   
        padding: 1rem;
        margin: 0 0 .5rem 1.6rem; 
    }
</style>