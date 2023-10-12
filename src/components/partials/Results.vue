<script>
import { store } from '../../data/store';
export default {
    name: 'Results',
    data(){
        store
    },
    computed:{
        getResults(){
            if(store.cardsList.length > 0){
                return `Found ${store.cardsList.length} cards`
            }
            return 'No cards found'
        }
    }
}
</script>


<template>
  <div>
    <p>{{ getResults }}</p>
  </div>
</template>


<style lang="scss" scoped>

div{
    width: 100%;
    background-color: black;
    padding: 20px;
    p{
        color: white;
        line-height: 100%;
        font-weight: bold;
        font-size: 1.3rem;
    }
}

</style>