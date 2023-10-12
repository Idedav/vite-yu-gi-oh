<script>
  export default {
    name:'Card'
  }
</script>


<template>
  <div class="card-container">
    <div class="dc-card">
      <img src="https://images.ygoprodeck.com/images/cards/34541863.jpg" alt="">
      <p>"A" CELL BREEDING DEVICE</p>
      <span>Alien</span>
    </div>
  </div>
</template>


<style lang="scss" scoped>
@use '../../scss/partials/vars' as *;
.card-container{
  width: calc(100% / 5);
  padding: 10px;
  .dc-card{
    width: 100%;
    text-align: center;
    background-color: $primary-color;
    padding-bottom: 15px;
    margin-bottom: 20px;
    img{
      width: 100%;
    }
    p{
      margin-top: 15px;
      font-weight: bold;
      font-size: 1.3rem;
      color: white;
    }
    span{
      font-size: 1.7rem;
    }
  }
}

</style>
