<script >

import AppHeader from './components/AppHeader.vue';
import AppNav from './components/AppNavbar.vue';
import AppSlider from './components/AppSlider.vue';

export default{

  components:{
    AppHeader,
    AppNav,
    AppSlider
  },

  Data(){
    return{
  
    }

  }
}

</script>

<template>

  <AppHeader></AppHeader>

  <AppNav></AppNav>

  <AppSlider></AppSlider>
  
</template>

<style lang="scss">
@use './style/general.scss' as *;

</style>
