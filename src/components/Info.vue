<template>
    <p v-if="estado_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidade!</p>
    <p>Utilizo as seguintes tecnlogias:</p>
    <ul>
        <li>PHP / Laravel</li>
        <li>Mysql</li>
        <li>Iniciando com vueJS</li>
    </ul>
    <p v-show="exibir">Mande uma mensagem para: {{ email}}</p>
</template>

<script>
export default {
    name: "Info",
    data() {
        return{
            estado_trabalhando: true,
            exibir: true,
            email: 'fabio@email.com'
        }
    }
}
</script>