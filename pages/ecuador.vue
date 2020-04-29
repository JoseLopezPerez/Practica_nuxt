<template>
  <div>
    <v-subheader class="text-center display-1	">Bienvenido a nuestro humilde pais</v-subheader >
    <v-subheader class=" body-1	">
      Si desea saber mas Información de nuestro País * 
      <v-btn  @click.stop="back()">
        Comenzemos 
      </v-btn>
    </v-subheader>
  </div>
</template>

<script>
export default {
  methods:{
    back(ruta){
      const rutaActual= '_capital'
      this.$router.push(`/ecuador/${rutaActual}`)
    }
  }
}
</script>

<style>

</style>
