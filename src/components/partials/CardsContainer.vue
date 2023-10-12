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
  <div class="cards-container my-5">
      <Results v-if="store.cardsReady === true"/>
      <Card 
      v-if="store.cardsReady === true"
      v-for="card in store.cardsList"
      :key="card.id"
      :image="card.card_images[0].image_url"
      :name="card.name"
      :archetype="card.archetype"
      />
      <Loader v-else/>
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
