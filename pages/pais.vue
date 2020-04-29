<template>
  <div class="light-blue accent-2 mx-auto">
    <v-btn to="/ecuador/_capital" color="primary">
      capital
    </v-btn>
    <v-card class="cyan darken-1 mx-auto" width="300">
      <v-subheader class="text-center grey darken-4" width="300"
        >Lista de las provincias</v-subheader
      >
      <v-card class="blue-grey lighten-1" width="300">
        <v-subheader>
          <v-list-item-group>
            <v-list-item v-for="(provincia, index) in provincia" :key="index">
              <v-list-item-icon> 
                <v-icon v-text="`${provincia.nombre}`">


                </v-icon>


              </v-list-item-icon>
            </v-list-item>
          </v-list-item-group>
        </v-subheader>
      </v-card>
    </v-card>

    <nuxt-child></nuxt-child>
  </div>
</template>

<script>
export default {
  data:()=>({
    provincia:[
      {nombre:'1.Guayaquil'},
      {nombre:'2.Cuenca'},
      {nombre:'3.Quito'}
    ]
  })
}
</script>

<style></style>
