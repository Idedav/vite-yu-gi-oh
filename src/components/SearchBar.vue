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
    <select name="" id="">
        <option selected>Search by archetype</option>
        <option value="alien">Alien</option>
    </select>
  </div>
</template>

<style lang="scss" scoped>

</style>