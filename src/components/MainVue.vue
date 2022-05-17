<template>

  <div id="main">
    <DischiVue />
  </div>

</template>

<script>
import DischiVue from './DischiVue.vue'

export default {
   name: "MainVue",
   components: {
     DischiVue
   }
}
</script>

<style lang="scss" scoped>
#main{
  height: 80vh;
  background-color: #1E2D3B;
}
</style>