<script >

import AppHeader from './components/AppHeader.vue';
import AppNav from './components/AppNavbar.vue';
import AppSlider from './components/AppSlider.vue';
import AppExample from './components/AppExample.vue';
import AppShowCase from './components/AppShowCase.vue';
import Citation from './components/Citation.vue';

export default{

  components:{
    AppHeader,
    AppNav,
    AppSlider,
    AppExample,
    AppShowCase,
    Citation
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

  <AppShowCase></AppShowCase>
  
  <Citation></Citation>
</template>

<style lang="scss">
@use './style/general.scss' as *;

</style>
