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
import News from './components/News.vue';
import Members from "./components/Members.vue";
import NewsLatters from "./components/NewsLatters.vue";
import AppFooter from './components/AppFooter.vue';

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
    Jumbotron,
    News,
    Members,
    NewsLatters,
    AppFooter

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

  <News></News>

  <Members></Members>

  <NewsLatters></NewsLatters>

  <AppFooter></AppFooter>
</template>

<style lang="scss">
@use './style/general.scss' as *;

</style>
