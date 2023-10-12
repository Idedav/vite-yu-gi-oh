<script>
import Header from './components/Header.vue';
import CardsContainer from './components/CardsContainer.vue';
  export default {
    name:'App',
    components:{
      Header,
      CardsContainer
    }
  }
</script>


<template>
  <Header />
  <CardsContainer />
</template>


<style lang="scss">

@use './scss/main.scss'

</style>
