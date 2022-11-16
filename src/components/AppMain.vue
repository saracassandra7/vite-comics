<script>
export default {
  name: 'AppMain'
}
</script>

<template>
  <main>
    <div class="jumbotron"></div>
  </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

main{

  .jumbotron{
    height: 350px;
    background-image: url(../src/assets/img/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: cover;
  }
}

</style>