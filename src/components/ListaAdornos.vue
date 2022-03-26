<template>
    <div class="list2">
    <h1>{{msg}}</h1>
          <h2>Adornos </h2>
    <dl>
        <dt class="adorn">Velas</dt>
        <dd class="adorn">- Vela personajes disney..........$150</dd>
        <dd class="adorn">- Vela personajes avengers.........$180</dd>
        <dd class="adorn">- Vela personajes numeros..........$100</dd>
        <dt class="adorn">Decoracion de nombres con cremas de colores</dt>
        <dd class="adorn">- Sabores combinados..................$100</dd>
        <dd class="adorn">- Un solo sabor ..................$25</dd>

    </dl>
    </div>
</template>

<script>
export default {
    name: 'ListaAdornos',
    props: {
        msg: String
    }
  
}
</script>
<style>
.list2{
float: left;
}
.adorn{
font-family: cursive;
}
</style>
