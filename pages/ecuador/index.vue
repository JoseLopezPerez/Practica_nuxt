<template>
  <div class="container">
    <v-row align="center" justify="center">
      <v-img
        src="https://especiales.elcomercio.com/documentos/2018/08/ecuador_independence.gif"
        max-height="200"
        max-width="200"
      ></v-img>
    </v-row>
    <v-row align="center" justify="center">
      <v-card>
        <v-subheader>
          * Bienvenido a Ecuador:
          <v-subheader>Lista de las Provincias del Ecuador:</v-subheader>
        </v-subheader>
      </v-card>
    </v-row>

    <v-card class="mx-auto" width="500" height="190">
      <v-list>
        <v-list-group class="blue-grey darken-3" v-for="(pais, index) in pais" :key="index">
          <v-list-item-content>
            <v-list-item-icon>
              <v-img class="mx-auto" max-height="70" max-width="70" :src="`${pais.avatar}`"></v-img>

              <v-icon class="mx-auto text-center " v-text="`${pais.nombre}`" ></v-icon>
            </v-list-item-icon>
          </v-list-item-content>
        </v-list-group>
        <h1>hahahahhaha</h1>
      </v-list>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    pais: [
      {
        nombre: 'Guayaquil',
        title: 'Guayaquil',
        avatar:
          'https://www.ecuavisa.com/sites/default/files/fotos/2019/06/13/guayaquil_0.jpg'
      },
      {
        nombre: 'Quito',
        title: 'Quito',
        avatar: 'https://media.metrolatam.com/2017/05/20/548306867-1200x600.jpg'
      },
      {
        nombre: 'Cuenca',
        title: 'Cuenca',
        avatar:
          'https://www.happygringo.com/wp-content/uploads/2020/01/cuenca-city-night-1200x675.jpg'
      }
    ]
  })
}
</script>

<style></style>
