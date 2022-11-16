<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import AppMain from './components/AppMain.vue';
import AppMenu from './components/AppMenu.vue'

export default {
  name: 'App',
  components:{
    AppHeader,
    AppFooter,
    AppMain,
    AppMenu
  }
}
</script>

<template>
  <AppHeader/>
  <AppMain/>
  <AppMenu/>
  <AppFooter/>
</template>

<style lang="scss">
 @use './styles/general'
</style>