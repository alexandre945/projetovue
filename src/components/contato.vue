<template>
    <div id="contato">
        <h1>Contatos</h1>
        <a href="https://web.whatsapp.com/send?fhone=5535998464219" target="_blank"><p>whatsap</p></a>
        <a href="https://facebook.com/Sousa Sousa" target="_blank"><p>Fecebook</p></a>
        <a href="https://instagram.com/alexandreroberto33" target="_blank"><p>Intagram</p></a>
        <p>Email:<br>alexandresousaroberto@gmail.com</p>
        <h2>projetos</h2>
        <a href="https://cadinoxequipamentos.vercel.app" target="_blank"><p>cadinox</p></a>
        <a href="https://loja-virtual-delta.vercel.app" target="_blank"><p>loja-virtual</p></a>
    </div>
</template>

 <script>
 export default {
     name:"contato"
 }
 </script>


   
   <style  scoped>
   #contato {
     color:peru;
     margin-left: 950px;
     margin-top: -300px;
     font-size: 15pt;
    transition:all 0.5s ease;
     
   
   }
   h1 {
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif; 
   }
   a {
        color:peru;
        text-decoration: none;
      
   }
   @media (max-width: 600px) {
#contato {
  margin-left: 15px;
  margin-top: 30px;
  font-size: 10pt;
}
h1 {
  font-size: 12pt;
}
   }
   
   </style>