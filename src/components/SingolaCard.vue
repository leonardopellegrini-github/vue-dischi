<template>
  <div>
    
  <div class="carta corpo card text-center">
   <div class=" card-body">
     <img :src="CardSing.poster" alt="Disco.title">
     <h5 class="card-title">{{CardSing.title}}</h5>
    <h5 class="card-title">{{CardSing.author}}</h5>
    <p class="card-text">{{CardSing.year}}</p>
    </div>
  </div>

  </div>
  
</template>

<script>
export default {
  name: 'SingolaCard',
  props:{
    CardSing: Object
  }
}
</script>

<style lang="scss" scoped>


img{
  width: 100%;
}

.carta{
  width: 18rem;
  background-color: transparent;
  color: white;
  background-color: transparent;
}

</style>