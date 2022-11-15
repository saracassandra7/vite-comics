<script>
export default {
  name: 'AppHeader',
  data(){
    return{
      menu:[
        {
          text: 'characters',
          href: '#',
          current: 'false'
        },
        {
          text: 'comics',
          href: '#',
          current: 'active'
        },
        {
          text: 'movies',
          href: '#',
          current: 'false'
        },
        {
          text: 'tv',
          href: '#',
          current: 'false'
        },
        {
          text: 'games',
          href: '#',
          current: 'false'
        },
        {
          text: 'collectibles',
          href: '#',
          current: 'false'
        },
        {
          text: 'videos',
          href: '#',
          current: 'false'
        },
        {
          text: 'fans',
          href: '#',
          current: 'false'
        },
        {
          text: 'news',
          href: '#',
          current: 'false'
        },
        {
          text: 'shop',
          href: '#',
          current: 'false'
        },
      ]
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
            <a :class="{'active': link.current== 'active'}" :href="link.href">{{link.text}}</a>
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
      border-bottom: 3px solid $main-blue;
     }

     &.active{
      color: $main-blue;

     }
    }
   }

  }
}


</style>