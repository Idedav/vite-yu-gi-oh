<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
  export default {
    name:'App',
    components:{
      Header,
      Main
    }
  }
</script>


<template>
  <Header />
  <Main />
</template>


<style lang="scss">

@use './scss/main.scss';
@use './scss/partials/vars' as *;

 body {
  background-color: $primary-color;
 }

</style>
