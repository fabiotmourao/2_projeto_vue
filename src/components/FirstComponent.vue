<template>
  <div>
    <h1>primeiro componente vue</h1>
    <p>Meu nome é {{ name }} e trabalho como {{ professional }}</p>
    <MultiplosEventos />
  </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue';
export default {
  name: "FirstComponent",
  components: {
    MultiplosEventos
  },
  data() {
    return {
      name: "Fábio",
      professional:"Programador"
    };
  },
};
</script>
