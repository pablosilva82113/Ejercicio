<template>
    <div class="lista">
    <h1>{{msg}}</h1>
         

    <h2 class="horario">Horarios </h2>
    <dl >
        <dt>Lunes a viernes</dt>
        <dd>- 9:00 AM a 8:00 PM</dd>
        
        <dt>Sabados y domingos</dt>
        <dd>- 10:00 AM a 6:00PM</dd>

    </dl>
     <br>
     <h3>Telefono 44567839</h3>
    
    </div>
</template>

<script>
export default {
  name: 'InfoGeneral',
    props: {
        msg: String
    }
  
}
</script>
<style>
.horario{
font-family: cursive;
}
</style>