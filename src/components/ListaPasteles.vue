<template>
    <div class="list">
     <!-- lista de pasteles -->
        <h1>{{msg}}</h1>
        <h2 class="listap">- Lista de pasteles</h2>
        <dt class="prod">Tipos de pasteles: de mantequilla</dt>
        <dd class="prod">Pasteles de Merengue...... $200</dd>
        <dd class="prod">Dacquoise...... $100</dd>
        <dd class="prod">Angel food...... $250 </dd>
        <dt class="prod">- Tipos de pasteles: de aceite</dt>
        <dd class="prod">Chiffon...... $100</dd>
        <dd class="prod">Pastel de zanahoria...... $100 </dd>
        <dd class="prod">Devil’s food...... $100 </dd>
    </div>
</template>

<script>
export default {
    name: 'ListaPasteles',
    props: {
        msg: String
    }
  
}
</script>

<style>
.list{
float: left;
}
.listap{
font-family: cursive;
}
.prod{
font-family: cursive;
}
 


</style>