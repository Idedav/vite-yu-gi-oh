<script>
  export default {
    name:'Header'
  }
</script>


<template>
  <header>
      <img src="/public/Yugioh_anime_logo.webp" alt="">
      <h1>Yu-Gi-Oh Api</h1>
  </header>
</template>


<style lang="scss" scoped>

header{
  display: flex;
  align-items: center;
  height: 100px;
  padding-left: 20px;
  background-color: white;
  img {
    width: 100px;
    margin-right: 15px;
  }
}

</style>
