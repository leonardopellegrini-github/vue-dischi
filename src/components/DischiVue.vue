<template>
  <div>
    <SingolaCard 
  :key="`disco-${index}`" v-for="(Disco, index) in elencoDischi"
    />
  </div>
</template>

<script>
import axios from 'axios';
import SingolaCard from './SingolaCard.vue';

export default {
  name: 'DischiVue',
  components: {
    SingolaCard
  },
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