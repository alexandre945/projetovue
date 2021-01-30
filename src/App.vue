<template>
  <div id="app">
    <cliente />
    <img src="./assets/xandy.jpg" alt="xandy.jpg">
    <mainn />
    <cadastro/>
    <contato/>
    <router-view></router-view>
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
}
img {
  height: 300px;
  width: 250px;
  margin-left: 500px;
  margin-top: -600px;
  
}

</style>
