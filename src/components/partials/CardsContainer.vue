<script>
import { store } from '../../data/store';
import Card from './Card.vue';

  export default {
    name:'CardsContainer',
    components:{
      Card
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
  width: 80%;
  background-color: white;
  padding: 50px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

</style>
