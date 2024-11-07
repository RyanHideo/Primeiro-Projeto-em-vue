<template>
  <v-app>
    <!-- Barra -->
    <v-app-bar color="primary">
      <v-btn icon @click="drawer = !drawer">
        <v-icon icon="mdi-menu"></v-icon>
      </v-btn>


      <v-app-bar-title>Cadastro de produtos </v-app-bar-title>
    </v-app-bar>

    <!-- Menu -->
    <v-navigation-drawer color="primary" v-model="drawer">
      <v-list-item to="/home" Link prepend-icon="mdi-home">
        Home
      </v-list-item>

      <v-list-item to="/Produtos" Link prepend-icon="mdi-shopping">
        Produtos
      </v-list-item>

      <v-list-item to="/Sair" Link prepend-icon="mdi-logout">
        Sair
      </v-list-item>

    </v-navigation-drawer>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script setup>
  import { ref } from 'vue'
  const drawer = ref(false)
</script>
