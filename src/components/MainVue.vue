<template>

  <div id="main">
    <div class="container">
        <DischiVue :genereDaCercare="genereDaCercare"/>
    </div>
  </div>

</template>

<script>
import DischiVue from './DischiVue.vue'

export default {
   name: "MainVue",

   components: {
     DischiVue
   },

   props:{
     genereDaCercare: String
   },
  
}
</script>

<style lang="scss" scoped>
#main{
  min-height: 80vh;
  background-color: #1E2D3B;
}

</style>