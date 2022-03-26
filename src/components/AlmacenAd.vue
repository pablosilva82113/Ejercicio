<template>
    <div>
         <h1>{{ msg }}</h1>
        <h1>Inventario Adornos </h1>
    <table border="1">
        <tr>
            <th>Vela personajes disney</th>
            <th>Vela personajes avengers</th>
            <th>Vela personajes numeros</th>
            <th>Decoracion de nombres con cremas de colores</th>
        </tr>
        <tr>
            <td>20 restantes</td>
            <td>10 restantes </td>
            <td>34 restantes</td>
            <td>24 cajas de sabores</td>
        </tr>
     
    </table>
    </div>
</template>

<script>
    export default {
          name: 'AlmacenAd',
          props: {
                 msg: String
          }
    }
</script>