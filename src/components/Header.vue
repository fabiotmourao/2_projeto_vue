<template>
  <div class="header">
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Projetos</a></li>
      <li><a href="#">Contatos</a></li>
      <li v-if="exibir"><a href="#">Meu Perfil</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Header",
  props:[
    "exibir",
  ]
};
</script>

<style scoped>
.header {
    padding: 1.5rem; 
}

ul {
  list-style: none;
  display: flex;
  /* background: #757272; */
}

li {
  margin: 1rem;
}

a {
  color: #ddd;
  text-decoration: none;
  transition: 0.5s;
}

a:hover {
  color: #40e0d0;
}
</style>
