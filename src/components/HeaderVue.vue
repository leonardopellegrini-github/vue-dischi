<template>

    <div id="header" class="d-flex d-flex justify-content-between align-items-center">

        <img src="@/img/pngegg.png" alt="Logo">
      
        <select v-model="cercaGenere" @change="$emit('cerca', cercaGenere)">
          <option value="">Seleziona un genere</option>
          <option value="Pop">Pop</option>
          <option value="Rock">Rock</option>
          <option value="Jazz">Jazz</option>
          <option value="Metal">Metal</option>
        </select>

    </div>
        


</template>

<script>

export default {
   name: "HeaderVue",
   data(){
    return{
      cercaGenere: '',
    }
  }
}
</script>

<style lang="scss" scoped>

#header{
  height: 20vh;
  background-color: #2E3A46;
  padding: 20px;
  img{
    width: 50px;
  }
  
}


</style>