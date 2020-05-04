<template>
  <div>
    PRODUCTOS
    <v-btn to="/productos/contenido">
      contenido
    </v-btn>

    <v-card class="mx-auto" max-width="300" tile>
      <v-list dense>
        <v-subheader>REPORTS</v-subheader>
        <v-list-item-group color="primary">
          <v-list-item v-for="(producto, index) in productos" :key="index">
            <v-list-item-icon>
              <v-icon v-text="`mdi-${producto.icon}`"></v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title   v-text="`model ${producto.ID}`"></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-card>

    <nuxt-child></nuxt-child>
  </div>
</template>

<script>
export default {
  data: () => ({
    productos: [
      { ID: ' 1', icon: 'clock' },
      { ID: ' 10', icon: 'account' },
      { ID: ' 100', icon: 'flag' }
    ]
  })
}
</script>

<style></style>
