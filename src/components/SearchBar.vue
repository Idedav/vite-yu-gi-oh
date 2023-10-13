<script>
import { store } from '../data/store';
export default {
    name:'SearchBar',
    data(){
        return{
            store
        }
    }
}
</script>


<template>
  <div class="container mt-5">
    <p>Search By Archetype:</p>
    <select v-model="store.archetypeToSearch" id="archetype-select">
        <option 
        v-for="(archetype, index) in store.archetypesList"
        :key="index"
        :value="archetype"
        :click="$emit('search')"
        >{{ archetype }}
        </option>
    </select>
  </div>
</template>

<style lang="scss" scoped>
    select{
        padding: 10px;
        font-size: 1.2rem;
    }
    p{
        font-weight: bold;
        font-size: 1.5rem;
    }
</style>