<script>
export default {
  name:'Header'
}
</script>


<template>
  <header class="d-flex align-items-center" >
    <img src="/public/Yugioh_anime_logo.webp" alt="">
    <h2>YU-GI-OH Api</h2>
  </header>
</template>



<style lang="scss" scoped>
@use '../scss/main' as *;
@use '../../scss/partials/variables' as *;

  header{
    width: $w-100;
    height: 100px;
    padding-left: 200px;
    h2 {
      font-size: 50px;
    }
  
    background-color: white;
    img {
      width: 130px;
      height: 40px;
      margin-right: 20px;
    }
  }
</style>