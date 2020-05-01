<template>
  <div>
       <ul>
         <h1 v-for="(nombreprincipal,index) in nombreprincipal" :key="index"
         v-text="`${{index}} `" > {{nombreprincipal.nombrecapitales}}</h1>
         <li v-text="`{{nombreprincipal.nombrecapitales}}`"> </li>
         <li>
           Guayaquil:1
         </li>
         <li> Quito : 2</li>
         <li> Cuenca: 3</li>
       </ul>
  </div>
</template>

<script>
export default {
  data:()=>({
    nombreprincipal:[
      {nombrecapitales: 'Capitales',nombreprincipalprovincia: 'Provincias'}
    ]
  })

}
</script>

<style>

</style>