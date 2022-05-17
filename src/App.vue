<template>

  <div>
    <HeaderVue />
    <MainVue />
  </div>

</template>

<script>
import HeaderVue from '@/components/HeaderVue.vue'
import MainVue from '@/components/MainVue.vue'

export default {
  name: 'App',
  components: {
    HeaderVue,
    MainVue
}
}
</script>

<style lang="scss">

*{
  box-sizing: border-box;
  padding: 0 auto;
  margin: 0 ;
}

</style>
