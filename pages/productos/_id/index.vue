<template>
  <div>
    <v-btn to="/productos">
      BACK
    </v-btn>

    <v-card class="mx-auto" max-width="322" max-height="322" color="primary">
      <h1 class="black--text font-italic">
        Producto ID: {{ $route.params.id }}
      </h1>
      <h2 class="green--text">Titulo: Matriz Hertz</h2>
      <label>Descripcion:</label>
      <v-col>
        <v-img
          height="200"
          width="310"
          src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
        >
        </v-img>
      </v-col>
    </v-card>
  </div>
</template>

<script>
export default {}
</script>

<style></style>
