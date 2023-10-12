<script>
import Card from './Card.vue';

  export default {
    name:'CardsContainer',
    components:{
      Card
    }
  }
</script>


<template>
  <div class="cards-container my-5">
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />

  </div>
</template>


<style lang="scss" scoped>

.cards-container{
  width: 80%;
  background-color: white;
  padding: 50px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

</style>
