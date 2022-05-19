<template>
  <div id="divline">
    <SingolaCard 
  :key="`Disco-${index}`" v-for="(Disco, index) in elencoDischi" :CardSing="Disco"
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
      elencoDischi: [],
      genereSelezionato: "",
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

    qualeGenere(valoreFiltro){
      this.valoreFiltro = valoreFiltro;
    }
  },

  /** 
  computed:{
    if (this.genereSelezionato === ''){
      return this.CardSing;
    },
    {return this.CardSing.filter(CardSing => CardSing.genre)}
  },
  */
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