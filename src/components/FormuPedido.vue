<template>
    <div>
        <h1>{{ msg }}</h1>
        <h2>Pedidos realizados</h2>

<table border="1">
<tr>
	<td>Nombre:</td><td><input type="text" name="nombreobtenido" id="nombreobtenido" ></td>
</tr>	
<tr>
	<td>telefono:</td><td><input type="text" name="telefonoobtenido" id="telefonoobtenido" ></td>
</tr>
<tr>
    <td>correo:</td><td><input type="text" name="correoobtenido" id="correoobtenido" ></td>
</tr>
<tr>
    <td>pastel:</td><td><input type="text" name="pastelobtenido" id="pastelobtenido" ></td>
</tr>
<tr>
    <td>adorno:</td><td><input type="text" name="adornoobtenido" id="adornoobtenido" ></td>
</tr>
</table>
    </div>
</template>

<script>
   export default {
       name: 'FormuPedido',
       props: {
           msg: String
       }
   } 
</script>