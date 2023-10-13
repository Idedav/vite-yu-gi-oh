<script>
import { store } from '../../data/store';
import Card from './Card.vue';
import Results from './Results.vue';

  export default {
    name:'CardsContainer',
    components:{
      Card,
      Results,
    },
    data(){
      return{
        store
      }
    }
  }
</script>


<template>
  <div class="container cards-container my-5">
      <Results />
      <Card 
      v-for="card in store.cardsList"
      :key="card.id"
      :image="card.card_images[0].image_url"
      :name="card.name"
      :archetype="card.archetype"
      />
  </div>
</template>


<style lang="scss" scoped>

.cards-container{
  min-height: 100%;
  background-color: white;
  padding: 50px;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

</style>
