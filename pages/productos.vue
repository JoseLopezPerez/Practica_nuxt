<template>
  <div>
      PRODUCTOS
      <v-btn to="/productos/contenido">
          contenido
      </v-btn>
       <v-btn to="/productos/10">
          producto 10
      </v-btn>
      <v-card class="mx-auto"
            max-width="322"
            max-height="322"
            color="primary"> 
    <h1 class="black--text font-italic">productos pruebas</h1>
    <h2 class="green--text">Titulo: Matriz Hertz</h2>
    <label>Descripcion:</label>
    <v-col>
        <v-img height="200" width="310" 
        src="https://cdn.vuetifyjs.com/images/cards/store.jpg">

        </v-img>
    </v-col>


      </v-card>
      <nuxt-child></nuxt-child>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>