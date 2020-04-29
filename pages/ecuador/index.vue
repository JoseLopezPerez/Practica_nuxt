<template>
  <div class="light-blue accent-2 mx-auto">
    <v-btn to="/ecuador/_capital" color="primary">
      capital {{ $route.params }}
    </v-btn>

    <v-card class="cyan darken-1 mx-auto" width="300">
      <v-subheader class="text-center grey darken-4" width="300"
        >Lista de las provincias</v-subheader
      >
      <v-card class=" mx-auto blue-grey lighten-1" width="300">
        <v-list-item-group>
          <v-list-item v-for="(provincia, index) in provincia" :key="index">
            <v-list-item-icon>
              <!-- <v-icon
                class="mx-auto"
                v-text="`${index+5}. ${provincia.nombre}`"
                width="300"
              >
              </v-icon> -->
              {{ index + 1 }}_ {{ provincia.nombre }}
            </v-list-item-icon>
          </v-list-item>
        </v-list-item-group>
      </v-card>
    </v-card>

    <nuxt-child></nuxt-child>
  </div>
</template>

<script>
export default {
  data: () => ({
    provincia: [
      { nombre: 'Guayas', route: 'guayas' },
      { nombre: '2.Cuenca', route: 'manabi' },
      { nombre: 'El Oro', route: 'el_oro' }
    ]
  }),
  methods: {
    back() {
      this.$router.push('/ecuador/guayaquil')
    }
  }
}
</script>

<style></style>
