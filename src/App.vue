<script >

import AppHeader from './components/AppHeader.vue';
import AppNav from './components/AppNavbar.vue';
import AppSlider from './components/AppSlider.vue';
import AppExample from './components/AppExample.vue';
import AppShowCase from './components/AppShowCase.vue';
import Citation from './components/Citation.vue';
import AppStats from './components/AppStats.vue';
import TopTrading from './components/TopTrading.vue';
import Jumbotron from './components/Jumbotron.vue';

export default{

  components:{
    AppHeader,
    AppNav,
    AppSlider,
    AppExample,
    AppShowCase,
    Citation,
    AppStats,
    TopTrading,
    Jumbotron

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

  <AppStats></AppStats>

  <TopTrading></TopTrading>

  <Jumbotron></Jumbotron>
</template>

<style lang="scss">
@use './style/general.scss' as *;

</style>
