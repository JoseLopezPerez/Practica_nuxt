<template>
  <div>
    NUMERO DE HABITANTES DE LA CAPITAL> {{ $route.params.capital }}
    250360 habitantess
    <v-btn color="success" @click.stop="back()">
      BACK
    </v-btn>
  </div>
</template>

<script>
export default {
  methods: {
    back(ruta) {
      const rutaActual = 'Azuay'
      this.$router.push(`/ecuador/${rutaActual}`)
      //template string
      //plantilla de texto
    }
  }
}
</script>

<style></style>
