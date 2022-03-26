<template>
    <div>
        <h1>{{ msg }}</h1>
     <form name="registro"> 
<table border="1">
<tr>
	<td>Nombre:</td><td><input type="text" name="nombre" id="nombre" ></td>
</tr>	
<tr>
	<td>telefono:</td><td><input type="text" name="telefono" id="telefono" ></td>
</tr>
<tr>
    <td>Correo:</td><td><input type="text" name="correo" id="correo" ></td>
</tr>
<tr>
    <td>Pastel:</td><td><input type="text" name="pastel" id="pastel" ></td>
</tr>
<tr>
    <td>Adorno:</td><td><input type="text" name="adorno" id="adorno" ></td>
</tr>
<tr>
	<td colspan ="5"><input type="button" name="btn1" value="Enviar" onclick="obtenerdatos()"></td>
</tr>
</table><br/><br/><br/>
</form> 
    </div>
</template>
<script>
    export default {
        name: 'Formulario',
        props: {
            msg: String
        }
    }
    methods: {
     function obtenerdatos()
	{
            var nombre = document.getElementById('nombre').value;
            var telefono = parseFloat(document.getElementById('telefono').value);
            var correo = document.getElementById('correo').value;
            var pastel = document.getElementById('pastel').value;
            var adorno = document.getElementById('adorno').value;
    
            document.registro.nombreobtenido.value = nombre;
            document.registro.telefonoobtenido.value = telefono;
            document.registro.correoobtenido.value = correo;
            document.registro.pastelobtenido.value = pastel;
            document.registro.adornoobtenido.value = adorno;

	}   
    }
</script>