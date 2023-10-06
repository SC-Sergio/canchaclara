<template>
    <v-app>
      <v-navigation-drawer app>
        <!-- Aquí irían los elementos de tu barra de navegación -->
      </v-navigation-drawer>
  
      <v-app-bar app>
        <v-toolbar-title>Sitio Web Cancha Clara</v-toolbar-title>
      </v-app-bar>
  
      <v-main>
        <!-- Cuerpo principal de tu página -->
        <v-container fluid>
          <v-row>
            <v-col cols="12">
              <v-jumbotron gradient="to bottom, rgba(100,115,201,1), rgba(126,87,194,1)">
                <h1>Bienvenido a la plataforma de reserva de canchas</h1>
                <v-btn color="pink" dark @click="goToReserve">Reservar ahora</v-btn>
              </v-jumbotron>
            </v-col>
          </v-row>
  
          <!-- Aquí puedes añadir más secciones a tu página de inicio -->
  
        </v-container>
      </v-main>
  
      <v-footer app>
        <span>&copy; {{ new Date().getFullYear() }} Sitio Web Cancha Clara</span>
      </v-footer>
    </v-app>
  </template>
  
  <script>
  export default {
    methods: {
      goToReserve() {
        this.$router.push("/reservas");
      }
    }
  };
  </script>
  
  <style scoped>
  /* Aquí puedes agregar estilos personalizados si lo necesitas */
  </style>
  