<script>
import CardsContainer from './partials/CardsContainer.vue';
import Loader from './partials/Loader.vue';
import { store } from '../data/store';
export default {
    name:'Main',
    components:{
        CardsContainer,
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
    <main class="d-flex justify-content-center align-items-center">
        <Loader v-if="store.isLoading"/>
        <CardsContainer v-else/>
    </main>
</template>


<style lang="scss" scoped>

main{
    min-height: 90vh;
}

</style>