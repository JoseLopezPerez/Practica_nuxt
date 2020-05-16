<template>
  <v-row justify="center" align="center">
    <v-col class="d-flex justify-center align-center" >
      <v-card width="500">
        <v-card-text class="text-center">
          <h2>{{ provinciaData.name }}</h2>
        </v-card-text>
        <v-card-text>
          <v-list dark color="grey darken-2" tile>
            <v-subheader
              >Lista de los Cantones del {{ provinciaData.name }}</v-subheader
            >
            <v-list-item
              v-for="canton in provinciaData"
              :key="canton.title"
              @click.stop=""
              
            ><h1>a</h1>
              <v-list-item-content>
                <v-list-item-title
                  class="text-center"
                  v-text="canton.name"
                ></v-list-item-title>
                
              </v-list-item-content>

              <v-list-item-avatar>
                <v-img :src="canton.avatar"></v-img>
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
  computed: {
    provinciaData() {
      return this.pais.find(provincia => provincia.id == this.provinciaId)
    },
    provinciaId() {
      return this.$route.params.provincia
    },
    cantonesData(){
      return this.pais.find(canton => canton.name == this.cantonName)
    },
  cantonName(){
    return this.$route.params.canton
  }
  },
  data: () => ({
    pais: [
      {
        id: 1,
        name: 'Guayas',
        route: '/guayas',
        avatar:
          'https://www.ecuavisa.com/sites/default/files/fotos/2019/06/13/guayaquil_0.jpg',
        cantones: [
          { name: 'Guayaquil', id: 11 },
          { name: 'Daule', id: 12 },
          { name: 'Samborondon', id: 12 }
        ]
      },
      {
        id: 2,
        name: 'El ORO',
        route: '/el_oro',
        avatar:
          'https://www.happygringo.com/wp-content/uploads/2020/01/cuenca-city-night-1200x675.jpg',
        cantones: [
          { name: 'Machala', id: 21 },
          { name: 'Piñas', id: 22 },
          { name: 'Zaruma', id: 23 }
        ]
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
