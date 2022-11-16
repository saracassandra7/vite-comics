<script>
import menu from "../assets/data/header-menu.js";

export default {
  name: 'AppHeader',
  data(){
    return{
      menu
    }
  }
}
</script>

<template>
  <header>
   <div class="container">
     <div class="logo">
      <img src="/dc-logo.png" alt="DC Logo">
     </div>
     <div class="menu">
      <nav>
        <ul>
          <li v-for="(link, index) in menu" :key="index">
            <a :class="{'active': link.current== 'true'}" :href="link.href">{{link.text}}</a>
          </li>

        </ul>
      </nav>
     </div>
   </div>
  </header>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;
header{
  height: 95px;

  .container{
   @include centerFlex('vertical');
   @include menuStyle();
   justify-content: space-between;

   img{
    width: 70px;
   }

   ul{
    @include centerFlex('horizontal');

    a{
     color: black;
     text-transform: uppercase;
     padding: 1.5rem .9rem 3.1rem .9rem;
     font-size: .85rem;
     font-weight: bold;
     display: inline-block;
     margin-bottom: 10px;

     &:hover, &.active{
      border-bottom: 4px solid $main-blue;
     }

     &.active{
      color: $main-blue;

     }
    }
   }

  }
}


</style>