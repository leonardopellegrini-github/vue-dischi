<template>
  <div id="divline">
    <SingolaCard 
  :key="`Disco-${index}`" v-for="(Disco, index) in dischiFiltrati" :CardSing="Disco" 
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
  props:{
     genereDaCercare: String
   },
  data(){
    return{
      apiUrl: 'https://flynn.boolean.careers/exercises/api/array/music',
      elencoDischi: [],
      
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
        this.elencoDischi = r.data.response;
      })
      .catch(e =>{
        console.log(e)
      })
    },

  },

  computed:{
    dischiFiltrati(){
      if(this.genereDaCercare === ""){
        return this.elencoDischi
      } else{
        return this.elencoDischi.filter(CardSing => CardSing.genre === this.genereDaCercare)
      }
    }
  }

}
</script>

<style lang="scss" scoped>
#divline{
  text-align: center;
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

</style>