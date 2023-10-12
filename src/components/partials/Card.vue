<script>
  export default {
    name:'Card',
    props:{
      image: String,
      name: String,
      archetype: String
    }
  }
</script>


<template>
  <div class="card-container">
    <div class="dc-card">
      <img :src="image" alt="">
      <p>{{ name }}</p>
      <span>{{ archetype }}</span>
    </div>
  </div>
</template>


<style lang="scss" scoped>
@use '../../scss/partials/vars' as *;
.card-container{
  width: calc(100% / 5);
  padding: 10px;
  height: 600px;
  .dc-card{
    width: 100%;
    height: 100%;
    text-align: center;
    background-color: $primary-color;
    margin-bottom: 20px;
    img{
      width: 100%;
    }
    p{
      margin-top: 15px;
      font-weight: bold;
      font-size: 1.3rem;
      color: white;
      padding: 5px 10px;
    }
    span{
      font-size: 1.5rem;
    }
  }
}

</style>
