<template>
  <v-row>
    <v-col class="d-flex justify-center align-center">
      <v-card dark width="500" color="white">
        <v-card-text class=" blue darken-4">
          <v-spacer></v-spacer>
          <h2>Bienvenido a Ecuador</h2>
        </v-card-text>
        <v-card-text style="height: 200px;">
          <v-img
            class="mx-auto"
            src="https://especiales.elcomercio.com/documentos/2018/08/ecuador_independence.gif"
            max-height="200"
            height="100%"
            contain=""
          ></v-img>
        </v-card-text>
        <v-card-text tile class="pt-0">
          <v-list dark color="grey darken-2" tile>
            <v-subheader>Lista de las Provincias del Ecuador</v-subheader>
            <v-list-item
              v-for="provincia in pais"
              :key="provincia.title"
              @click.stop=""
              :to="`ecuador/${provincia.id}`"
            >
              <v-list-item-content>
                <v-list-item-title
                  class="text-center"
                  v-text="provincia.name"
                ></v-list-item-title>
              </v-list-item-content>

              <v-list-item-avatar>
                <v-img :src="provincia.avatar"></v-img>
              </v-list-item-avatar>
            </v-list-item>
          </v-list>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    pais: [
      {
        id: 1,
        name: 'Guayas',
        route: '/guayas',
        avatar:
          'https://www.ecuavisa.com/sites/default/files/fotos/2019/06/13/guayaquil_0.jpg',
        cantones: [
          { name: 'Guayaquil' },
          { name: 'Daule' },
          { name: 'Samborondon' }
        ]
      },
      {
        id: 2,
        name: 'El ORO',
        route: '/el_oro',
        avatar:
          'https://www.happygringo.com/wp-content/uploads/2020/01/cuenca-city-night-1200x675.jpg',
        cantones: [{ name: 'Machala' }, { name: 'Piñas' }, { name: 'Zaruma' }]
      },
      {
        id: 3,
        name: 'Manabi',
        route: '/manabi',
        avatar:
          'https://media.metrolatam.com/2017/05/20/548306867-1200x600.jpg',
        cantones: [
          { name: 'Manta' },
          { name: 'Montecristi' },
          { name: 'Portoviejo' }
        ]
      }
    ]
  })
}
</script>

<style></style>
