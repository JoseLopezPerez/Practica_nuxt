<template>
  <div>
    <ul>
      <h1
        v-for="(nombreprincipal, index) in nombreprincipal"
        :key="index"
        v-text="
          `${nombreprincipal.nombrecapitales} - ${nombreprincipal.nombreprincipalprovincia}`"></h1>
      <li v-for="(provinciasycapitales, index) in provinciasycapitales" :key="index" > {{provinciasycapitales.capitales}}  - 
        {{provinciasycapitales.provinciass}} </li>
    </ul>
  </div>
</template>

<script>
export default {
  data: () => ({
    nombreprincipal: [
      {
        nombrecapitales: 'Capitales',
        nombreprincipalprovincia: 'Provincias',}
        ],
<<<<<<< HEAD
        // CORREGIR EL OBJETO

        
=======
        // CORREGIR EL OBJETO, anidar los elementos
>>>>>>> 435ecb68adacf612509acc6cca6ba0930a4c452c
        provinciasycapitales:[
          {capitales:'Guayaquil' ,provinciass:'Guayas'},
          {capitales:'Quito ' ,provinciass:'Quito'},
          {capitales:'Azuay ' ,provinciass:'Azuay'}
        ]

  })
}
</script>

<style></style>