<template>
  <div>
    <h1>primeiro componente vue</h1>
    <p>Meu nome é {{ name }} e trabalho como {{ professional }}</p>
  </div>
</template>

<script>
export default {
  name: "FirstComponent",
  data() {
    return {
      name: "Fábio",
      professional:"Programador"
    };
  },
};
</script>
