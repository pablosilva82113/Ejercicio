<template>
    <div>
        <h1>{{ msg }}</h1>
        <h1>Inventario </h1>
    <table border="1">
        <tr>
            <th>Leche</th>
            <th>Huevo</th>
            <th>Mantequilla</th>
            <th>Chocolate</th>
        </tr>
        <tr>
            <td>50 litros</td>
            <td>60 kg</td>
            <td>20 kg</td>
            <td>20 kg</td>
        </tr>
     
    </table>
    </div>
</template>

<script>
    export default {
         name: 'AlmacenIn',
         props: {
              msg: String
         }
    }
</script>