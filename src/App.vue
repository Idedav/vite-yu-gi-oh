<script>
import axios from 'axios';
import { store } from './data/store';
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import SearchBar from './components/SearchBar.vue';
  export default {
    name:'App',
    components:{
      Header,
      Main,
      SearchBar
    },
    data(){
      return{
        store
      }
    },
    methods:{
      getApi(){
        store.isLoading = true;
        const url = store.archetypeToSearch != "" ? store.apiUrl + "?archetype=" + store.archetypeToSearch : store.apiUrl;
          axios.get(url)
          .then(result =>{
  
            store.cardsList = result.data.data;
            store.isLoading = false
            store.cardsList.forEach(card =>{
              if(!store.archetypesList.includes(card.archetype)){
                if(card.archetype){
                  store.archetypesList.push(card.archetype)
                }
              }
            })
          })
          .catch(error =>{
            console.log(error);
          })
      }
    },
    mounted(){
        this.getApi();
      }
  }
</script>


<template>
  <Header />
  <SearchBar :search="getApi()"/>
  <Main />
</template>


<style lang="scss">

@use './scss/main.scss';
@use './scss/partials/vars' as *;

 body {
  background-color: $primary-color;
 }

</style>
