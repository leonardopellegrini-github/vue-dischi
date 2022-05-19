<template>
  
      <div class="col-3 carta">
        <img class="thumb" :src="CardSing.poster" alt="Disco.title">
        <div>
          <h5>{{CardSing.title}}</h5>
          <h5>{{CardSing.author}}</h5>
          <p>{{CardSing.year}}</p>
          <p>{{CardSing.genre}}</p>
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




.carta{
  background-color: transparent;
  color: white;
  background-color: transparent;
  
  img{
  width: 100%;
  max-height: 150px;
  max-width: 150px;
  }
}

</style>