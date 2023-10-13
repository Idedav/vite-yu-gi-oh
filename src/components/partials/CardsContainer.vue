<script>
import { store } from '../../data/store';
import Card from './Card.vue';
import Loader from './Loader.vue';
import Results from './Results.vue';

  export default {
    name:'CardsContainer',
    components:{
      Card,
      Results,
      Loader
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
    <Loader v-if="store.isLoading"/>
      <Results v-else/>
      <Card 
      v-if="!store.isLoading"
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
  justify-content: center;
  align-items: center;
}

</style>
