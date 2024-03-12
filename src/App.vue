<script >

import AppHeader from './components/AppHeader.vue';
import AppNav from './components/AppNavbar.vue';
import AppSlider from './components/AppSlider.vue';
import AppExample from './components/AppExample.vue';

export default{

  components:{
    AppHeader,
    AppNav,
    AppSlider,
    AppExample
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

  <AppExample></AppExample>
  
</template>

<style lang="scss">
@use './style/general.scss' as *;

</style>
