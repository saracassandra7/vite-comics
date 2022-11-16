<script>
import menu from '../assets/data/menu.js'

export default {
  name: 'AppMenu',

  data(){
    return{
      menu
    }
  }
}
</script>

<template>
<div class="container-blue">
  <div class="container">
    <div v-for="(link, index) in menu" :key="index" class="item">
      <div class="img-container">
        <img :src="link.imgPath" :alt="link.text">
      </div>
      <span>{{link.text}}</span>
    </div>

    
  </div>
</div>
  
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

.container-blue{
  background-color: $main-blue;
  height: 140px;
  color: white;
  @include centerFlex('vertical');

  .container{
    @include centerFlex('vertical');
    justify-content: space-evenly;
  }

  .item{
    @include centerFlex('vertical');
    cursor: pointer;
  }

  .img-container{
    width: 50px;
    height: 60px;
    margin-right: 10px;

    img{
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
    
  }

  span{
    text-transform: uppercase;
    font-size: .9rem;
  }
}


</style>