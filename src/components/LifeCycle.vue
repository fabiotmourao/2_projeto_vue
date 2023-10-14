<template>
  <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
export default {
  name: "LifeCycle",
  data() {
    return {
      nome: "Ainda não sei",
    };
  },
  created() {
    setTimeout(() => {
      this.nome = " Fábio";
    }, 1000);
  },
  mounted() {
    setTimeout(() => {
      this.nome = "Fábio Teixeira";
    }, 3000);

    this.lifeCycle();
  },
  methods: {
    lifeCycle() {
      console.log('Executou');
    }
  }
};
</script>
