<template>
  <div>
    <ul>
      <h1
        v-for="(nombreprincipal, index) in nombreprincipal"
        :key="index"
        v-text="
          `${nombreprincipal.nombrecapitales} - ${nombreprincipal.nombreprincipalprovincia}`
        "
      ></h1>
      <li
        v-for="(provinciasycapitales, index) in provinciasycapitales"
        :key="index"
      >
        {{ provinciasycapitales.capitales }} -
        {{ provinciasycapitales.provinciass }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data: () => ({
    nombreprincipal: [
      {
        nombrecapitales: 'Capitales',
<<<<<<< HEAD
        nombreprincipalprovincia: 'Provincias'
      }
    ],
    // CORREGIR EL OBJETO
    provinciasycapitales: [
      { capitales: 'Guayaquil', provinciass: 'Guayas' },
      { capitales: 'Quito ', provinciass: 'Quito' },
      { capitales: 'Azuay ', provinciass: 'Azuay' }
    ],
    provincias: [
      { provinciass: 'Guayas' },
      { provinciass: 'Quito' },
      { provinciass: 'Azuay' }
    ]
=======
        nombreprincipalprovincia: 'Provincias',}
        ],
        // CORREGIR EL OBJETO ANINADO EN PROVINCIAS        
        provinciasycapitales:[
          {capitales:'Guayaquil' ,provinciass:'Guayas'},
          {capitales:'Quito ' ,provinciass:'Quito'},
          {capitales:'Azuay ' ,provinciass:'Azuay'}
        ]

>>>>>>> 60fb8d4a0ea165848c09d384011b2de78775feae
  })
}
</script>

<style></style>
