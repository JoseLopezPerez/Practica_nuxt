<template>
  <div>
      BIENVENIDO A LA CAPITAL (canton) {{$route.params.capital}} de la provincia de {{$route.params.provincia}}

      <v-btn to="/pais">
       regresar a la ruta Principal llamada Pais
      </v-btn>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>