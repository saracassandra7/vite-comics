<script>
import ComicsCard from './ComicsCard.vue';
import comics from '../assets/data/dc-comics'

export default {
  name: 'AppMain',
  components:{
    ComicsCard
  },
  data(){
    return{
      comics
    }
  }
}
</script>

<template>
  <main>
    <div class="jumbotron"></div>
    <div class="container">
      <div class="btn">
        <h3>CURRENT SERIES</h3>
      </div>

      <div class="comics">
        <ComicsCard v-for="(comic, index) in comics" :key="index" :comicTitle="comic.series" :comicImg="comic.thumb"/>

      </div>

    </div>


  </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

main{
  background-color: #1c1c1c;
  color: #f5e8fc;

  .jumbotron{
    height: 350px;
    background-image: url(../src/assets/img/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: cover;
  }

  .comics{
    display: flex;
    flex-wrap: wrap;
  }
}

</style>