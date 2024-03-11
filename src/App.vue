<script >

import AppHeader from './components/AppHeader.vue';
import AppNav from './components/AppNavbar.vue';

export default{

  components:{
    AppHeader,
    AppNav
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
  
</template>

<style lang="scss">
@use './style/general.scss' as *;

</style>
