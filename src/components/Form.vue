<template>
  <h2>Meu Formulário:</h2>
  <form action="" @submit="enviarForm($event)">
    <div>
           <input type="text" v-model="name">
        <!-- <InputText /> -->
    </div>
    <div>
           <input type="text" v-model="email">

        <!-- <InputText /> -->
    </div>
    <div>
        <Submit />
    </div>
  </form>
</template>

<script>
import InputText from './form/InputText.vue';
import Submit from './form/Submit.vue';

export default {
  name: "Form",
  data() {
    return{
      name: "",
      email: ""
    }
  },
  components: {
    InputText,
    Submit,
  },
  methods: {
    enviarForm(e){
      e.preventDefault();

      const name = this.name;
      const email = this.email;
      console.log("Formulario enviado!");
      console.log("Meu nome é: " + name + " ");
      console.log("E-mail de contato  é: " + email + " ");
    }
  }
};
</script>

<style>
  form {
    margin-bottom: 25rem;
  }
</style>