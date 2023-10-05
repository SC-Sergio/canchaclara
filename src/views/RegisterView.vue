<template>
<div>
<h1>Registro de Usuario</h1>
<form>
    <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" name="nombre" required><br>

        <label for="correo">Correo electrónico:</label>
        <input type="email" id="correo" name="correo" required><br>

        <label for="contrasena">Contraseña:</label>
        <input type="password" id="contrasena" name="contrasena" required><br>

        <!-- Agrega aquí más campos según tus necesidades -->

        <input type="submit" value="Registrarse">

</form>


</div>
</template>

<script setup>


</script>

<style scoped>

</style>