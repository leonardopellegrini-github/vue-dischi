<template>

  <div>
    <HeaderVue @cerca="cerca"/>
    <MainVue :genereDaCercare="genereDaCercare"/>
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
  },
  data(){
    return{
      genereDaCercare: '',
    }
  },
  methods:{
    cerca(genereDaCercare){
      this.genereDaCercare = genereDaCercare;
      console.log(genereDaCercare);
    }
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
