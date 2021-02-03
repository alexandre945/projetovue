<template>
    <div> 
            <h2>ENTRE EM CONTATO:</h2>
          
            
       <form action="https://formspree.io/xandylambamg@hotmail.com" method="POST">
               
                <label for="">Nome</label><br>
                <input  v-model="nome" @change="$v.nome.$touch()" type="text" ><br>
                 <p v-if="$v.nome.$error">este campo é obrigatorio.</p> 
            
                <label for="">Email</label><br>
                <input v-model="email" @change="$v.email.$touch()" type="tex" > <br>
                 <p v-if="$v.email.$error">este campo é obrigatorio.</p> 

                  <label for="">EMPPRESA</label><br>
                <input v-model="empresa" @change="$v.empresa.$touch()" type="tex" > <br>
                 <p v-if="$v.email.$error">este campo é obrigatorio.</p> 


                <label for="">Mensagen</label><br>
                <textarea v-model="mensagem"  @change="$v.mensagem.$touch()" type="text" ></textarea><br>
                  <p v-if="$v.mensagem.$error">este campo é obrigatorio.</p> 

            <div id="tex"> 
                Nome: {{ nome }}<br>
                Email:{{ email }}<br>
                Empresa:{{ empresa }}<br>
                Mensagem:{{ mensagem }}<br>
               
            </div>
 <button type="submit" @click.prevent="login()">ENVIAR</button><br>

        </form>

    </div>
</template>
<script>
import { required,email }  from 'vuelidate/lib/validators';
export default {
    nome: "required", 
    data() {
        return {
            nome:"",
            email:"",
            mensagem:"",
            empresa:"",

         
            }
        },
         validations: {
                nome: { required } ,
                email: { required,email },
                mensagem: { required },
                empresa: { required},
                
            },
 methods: {
   

    login(){
        if( !this.$v.invalid ) {
            alert('mensagem enviada com sucesso!')
        }else{
            this.$v.$tuoch();
        }
     }
 }, 

}
</script>
<style scoped>
h2 {
    color:chocolate
}
input {
    background-color: black;
    color: chocolate;
    height: 40px;
    width: 250px;
     border: solid 2px chocolate;
     font-size: 15pt;
}
label {
      background-color: black;
    color: chocolate;
}
textarea {
    background-color: black;
    color: chocolate;
    border: solid 2px chocolate;
    width: 250px;
    font-size: 15pt;
}
#tex {
    color: chocolate; 
    font-size: 15pt;
   
}
button {
    background-color: black;
    color: chocolate;
    border: solid 2px chocolate;  
}
lU {
      color: chocolate; 
}
#li {
    background-color: azure;
    height: 200px;
}
p {
    color: white;
}
</style>