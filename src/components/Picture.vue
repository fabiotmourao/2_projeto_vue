<template>
  <div>
    <img :src="avatar" :alt="description" />
    <MudarImagem  @mudar-imagem="trocarImagem"/>
  </div>
</template>

<script>
import MudarImagem from "./MudarImagem.vue";    

export default {
  name: "Picture",
  components: {
    MudarImagem
  },
  data() {
    return {
      // Initialize avatar with a default image
      avatar: "/img/avatar.png",
      
      avatar1: "/img/avatar.png",
      avatar2: "/img/avatar2.png",
      description: "Avatar do usuário",
    };
  },
  methods: {      
      trocarImagem(){
       const avatar1 = this.avatar1; 
       const avatar2 = this.avatar2; 

       if (this.avatar === avatar1){
            this.avatar = avatar2   
       } else {
            this.avatar = avatar1   
       }
    }
  }
};
</script>
