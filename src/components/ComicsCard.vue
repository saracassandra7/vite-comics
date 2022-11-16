<script>

export default {
  name: 'ComicsCard',

  props:{
    comicImg: String,
    comicTitle: String
  }
}
</script>

<template>
<div class="card">
  <div class="card-img">
    <img :src="comicImg" :alt="comicTitle">
  </div>
  
  <span>{{comicTitle}}</span>
</div>
  
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

.card{
  width: calc(100% / 6 - 5px);
  margin-bottom: 20px;

  .card-img{
    width: 150px;
    height: 150px;
    overflow: hidden;

    img{
      max-width: 100%;
    }
  }

  span{
    text-transform: uppercase;
    display: inline-block;
    margin: 15px 0;
    font-size: .9rem;
  }
}

</style>