<template>
<div id="formgrup"> 
          
    <div id="forme"> 
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
                    <button type="submit" @click.prevent="login()">ENVIAR</button><br>

        </form>
    </div>
            <div id="tex"> 
                 Nome: {{ nome }}<br><br><br>
                Email: {{ email }}<br><br><br>
                Empresa: {{ empresa }}<br><br><br>
                Mensagem: {{ mensagem }}<br><br><br>
               
            </div>
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
#forme {
    padding-left: 20px;
}
#formgrup {
    display: flex;
}
h2 {
    color:peru;
    padding-left: 20px;
}
input {
    background-color: black;
    color:peru;
    height: 40px;
    width: 250px;
    border: solid 2px peru;
    font-size: 15pt;
    cursor: pointer;
    border-radius: 8px;
}
label {
    background-color: black;
   color:peru;
}
textarea {
    background-color: black;
    color:peru;
    border: solid 2px peru;
    width: 250px;
    font-size: 15pt;
    cursor: pointer;
     border-radius: 8px;
}
#tex {
 color:peru;
font-size: 15pt;
margin-top: 90px;
margin-left: 100px;

}
button {
    background-color: black;
     color:peru;
    border: solid 2px peru;
    cursor: pointer;  
}
lU {
       color:peru;
}
#li {
    background-color: azure;
    height: 200px;
}
p {
    color: white;
}
button {
    color:peru;
}
</style>