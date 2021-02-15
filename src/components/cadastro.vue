<template>
<div id="formgrup"> 
          
    <div id="forme"> 
             <h2>ENTRE EM CONTATO:</h2>
              <form action="https://api.staticforms.xyz/submit" method="post">
                    <input v-model="nome" type="text" name="name" placeholder="seu nome:"><br>
                    <input v-model="email" type="text" name="email" placeholder="seu Email:" /><br>
                    <textarea v-model="mensagem" name="message" placeholder="deixe,sua mensagem:"></textarea><br>
                    <input type="text" name="honeypot" style="display:none">
                    <input type="hidden" name="accessKey" value="2811af00-0456-4c02-a5fb-adb2057f2630">
                    <input type="hidden" name="replyTo" value="xandylamabamg@hotmail.com">
                    <input type="hidden" name="redirectTo" value="https://projetovue.vercel.app">
                    <input type="submit" value.prevente="Submit" />
            </form>
    </div>
            <div id="tex"> 
                 Nome: {{ nome }}<br><br><br>
                Email: {{ email }}<br><br><br>
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
         

            }
        },
         validations: {
                nome: { required } ,
                email: { required,email },
                mensagem: { required },
                
                
            },
 methods: {
   

    login(){
        if( !this.$v.invalid ) {
            alert('mensagem enviada com sucesso!');
            this. nome =  "";
            this.email = "";
            this.mensagem = "";
        }else{
            this.$v.$tuoch();
            
        }

    },

 }, 
 
}
</script>
<style scoped>
#forme {
     padding-left: 20px; 
     margin-top: 30px;
}
#formgrup {
     display: flex; 
       color:peru;
       background-color:black;

}
h2 {
    color:peru;
    padding-left: 20px;
}
input {
     background-color:black; 
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
 background-color:black;
font-size: 15pt;
margin-top: 90px;
margin-left: 100px;

}
button {
    background-color: black;
     color:peru;
    border: solid 2px peru;
    cursor: pointer; 
    margin-left: 100px; 
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
::placeholder {
     color:peru;
}
@media (max-width:600px) {
    #formgrup {
        margin-top: 900px;
    }
        #tex {
          margin-left: -250px;
            margin-top: 295px;
            padding: 0px;

        }
}
</style>