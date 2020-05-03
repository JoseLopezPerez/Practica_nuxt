<template>
  <div>
    <v-card>
      <v-card-text>
        PRUEBA
      </v-card-text>
      <v-card-text>
        <v-subheader>
          <ul class="blue lighten-2  ">
            <h1
              class="text-center"
              v-for="(nombreprincipal, index) in nombreprincipal"
              :key="index"
              v-text="
                `${nombreprincipal.nombrecapitales} - ${nombreprincipal.nombreprincipalprovincia}`
              "
            ></h1>

            <li
              v-for="(provinciasycapitales, i) in provinciasycapitales"
              :key="i"
            >
              {{ provinciasycapitales.capitales }} -
              {{ provinciasycapitales.provinciass }}
            </li>
          </ul>
        </v-subheader>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    nombreprincipal: [
      {
        nombrecapitales: 'Capitales',
        nombreprincipalprovincia: 'Provincias'
      }
    ],
    procesadores: [
      {
        marca: 'Intel',
        año: 1950,
        modelos: [
          { nombre: 'i3', caracteristicas: ['hyperThreading'] },
          { nombre: 'i5', caracteristicas: ['hyperThreading', 'turbo boost'] }
        ]
      }
    ],
    pais: {
      nombre: 'Ecuador',
      id: 1,
      superficie: 140000,
      provincias: [
        {
          nombre: 'Guayas',
          superficie: 86000,
          cantones: [
            { nombre: 'Guayaquil', parroquias: [{ nombre: 'Tarqui' }] },
            { nombre: 'Samborondon' },
            { nombre: 'Daule' }
          ]
        },
        {
          nombre: 'Azuay',
          superficie: 20000
        }
      ]
    },
    provinciasycapitales: [
      { capitales: 'Guayaquil', provinciass: 'Guayas' },
      { capitales: 'Quito ', provinciass: 'Quito' },
      { capitales: 'Azuay ', provinciass: 'Azuay' }
    ]
  })
}
</script>

<style></style>
