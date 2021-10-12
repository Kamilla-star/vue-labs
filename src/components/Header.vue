<template>
  <v-container>
    <v-toolbar dense fixed>
    <v-toolbar-side-icon></v-toolbar-side-icon>
    <v-toolbar-title>Камилла</v-toolbar-title>
    <v-spacer></v-spacer>

    <v-text-field
        hide-details
        prepend-icon="mdi-magnify"
        single-line
      ></v-text-field>
    <v-spacer></v-spacer>

    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn text><router-link class="link" to="/">Главная</router-link></v-btn>
        <v-btn text><router-link class="link" to="/news">Новости</router-link></v-btn>
        <v-btn text><router-link class="link" to="/gallery">Галерея</router-link></v-btn>
    </v-toolbar-items>
  </v-toolbar>
  </v-container>
</template>

<script>
  
  export default {
    data () {
      return {
        
      }
    },
  }
</script>

<style scoped>
  .link {
    color: black;
    outline: none;
    text-decoration: none;
  }
</style>