<template>
  <div id="app">
      <cliente />
      <contato />
      <img src="./assets/xandy3.jpg" alt="alex.jpg"> 
      
      <mainn />
      <cadastro/>
  </div>
</template>
<script>
import cliente from "./components/cliente.vue";
import mainn from "./components/mainn.vue";
import cadastro from "./components/cadastro.vue";
import contato from "./components/contato.vue";

export default {
    name: "App",
    components: {
    cliente,
    mainn,
    cadastro,
    contato,
   
  }
}
</script>

<style>
#app {
    background-color: black;
    border: solid 5px peru;
    
}
img {
  height: 313px;
  width: 280px;
  margin-left: 510px;
  margin-top: -600px; 
  margin-bottom: 100px;
 padding-top: 0px;
 border: solid 2px peru;
 text-align: center;
  
}
@media (max-width: 600px) {
  #app {
  width: 400px;
  height: 2000px;
  }
  img {
    margin-left: 15px;
    margin-top: 8px;
    height: 200px;
    width: 180px;
  }
}

</style>      