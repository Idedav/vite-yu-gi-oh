<script>
export default {
    name: 'Loader'
}
</script>


<template>
  <div class="container d-flex justify-content-center">
    <div class="card-wrapper">
      <img class="card" src="/public/front.jpg" alt="" />
      <img class="card card-back" src="/public/back.jpg" alt="" />
    </div>
  </div>
</template>


<style lang="scss" scoped>
@use '../../scss/partials/vars' as *;

@keyframes cardFlip {
  0% {
    transform: rotateY(0deg);
  }
  50% {
    transform: rotateY(180deg);
  }
  100% {
    transform: rotateY(0deg);
  }
}

.card-wrapper {
  position: relative;
  transform-style: preserve-3d;
  animation: cardFlip 3s ease-in-out infinite;
  width: 200px;
  height: 300px;
}

.card {
  position: absolute;
  backface-visibility: hidden;
  width: 200px;
  height: 300px;
}

.card-back {
  transform: rotateY(180deg);
}
   
    
</style>