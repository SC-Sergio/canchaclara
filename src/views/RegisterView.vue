<template>
    <div>
      <!-- Formulario de registro -->
      <form @submit.prevent="registerUser">
        <input v-model="user.name" placeholder="Nombre" required>
        <input v-model="user.email" type="email" placeholder="Correo electrónico" required>
        <input v-model="user.password" type="password" placeholder="Contraseña" required>
        <button type="submit">Registrar</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        user: {
          name: '',
          email: '',
          password: ''
        }
      };
    },
    methods: {
      async registerUser() {
        try {
          // Validación de datos del formulario (puede ser más exhaustiva)
          if (!this.user.name || !this.user.email || !this.user.password) {
            alert('Por favor, completa todos los campos.');
            return;
          }
  
          // Aquí, harías una llamada a tu API o backend para registrar al usuario
          const response = await this.$axios.post('/api/register', this.user);
          
          if (response.data.success) {
            // Informar al usuario que se ha registrado con éxito
            alert('Registro exitoso. Por favor, verifica tu correo.');
            this.user = { name: '', email: '', password: '' }; // Limpiar el formulario
          } else {
            // Mostrar un error al usuario si algo va mal
            alert('Error: ' + response.data.message);
          }
        } catch (error) {
          console.error('Ha ocurrido un error durante el registro:', error);
          alert('Error durante el registro. Intenta de nuevo.');
        }
      }
    }
  };
  </script>
  