<template>

    <div id="stek">
        <h1>Skills:</h1> 
        <p>HTML/<br>85%</p><br>
        <p>CSS/<br>68%</p>
        <p>Java Script(JS)/<br>45%</p>
        <p>Vue Js/<br>35%</p>
        <p>github/<br>60%</p>
        <p>Git/<br>70%</p>
        <p>mysql/<br>25%</p>
        <p>Node JS/<br>35%</p>
        <P>Squelite/<br>30%</p>
        <p>Foco/<br>110%</p>
        
        
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
h1 {
    color: peru;
    padding-left: 20px; 
    
    
}
p {
 color: peru;
 font-size: 20pt;
 padding-left: 25px;
  
}
#stek {
   display: flex;
   text-align: center;
    margin-left: 0px;
    border: solid 2px peru;
      
}
@media (max-width: 600px) {
  #stek {
      /* display: none; */
      margin-top: -100px;
      margin-left: -260px;
      height: 70px;
      display: block;
  }  
}
</style>
