<template>
  <Header />
  <FirstComponent />
  <LifeCycle />
  <Pessoa />
</template>

<script>
import Header from "./components/Header.vue";
import FirstComponent from "./components/FirstComponent.vue";
import LifeCycle from './components/LifeCycle.vue';
import Pessoa from './components/Pessoa.vue'

export default {
  name: "App",
  components: {
    Header,
    FirstComponent,
    LifeCycle,
    Pessoa,
  },
};
</script>

<style>
  * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
  }

  body{
    background-color: #333;
    color: #fff;
  }

  a {
    color: red;
  }

  .teste{ 
    background-color: #000;
  }
</style>
