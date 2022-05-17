<template>
  <div>
    DISCHI
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'DischiVue',
  data(){
    return{
      apiUrl: 'https://flynn.boolean.careers/exercises/api/array/music',
      elencoDischi: []
    }
  },
  mounted(){
    this.getApi();
  },
  methods:{
    getApi(){
      axios.get(this.apiUrl)
      .then(r =>{
        console.log(r.data)
      })
      .catch(e =>{
        console.log(e)
      })
    }
  }
}
</script>

<style>

</style>