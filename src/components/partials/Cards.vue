
<script>
export default {
  name:'Cards',
  props:{
    img: String,
    name: String,
    type: String
  }
}
</script>


<template>
  <div class="my_col">
    <div class="my_card">
      <img :src="img">
      <h6>{{ name }}</h6>
      <p>{{ type }}</p>
    </div>
  </div>
</template>



<style lang="scss" scoped>
@use '../../../scss/partials/variables' as *;
@use '../../../scss/partials/general' as *;


.my_col {
  width: 20%;
  margin-bottom: 15px;
}
.my_card{
  background-color: $bg-orange;
  text-align: center;
  height: 100%;
  img{
    max-width:100% ;
    margin-bottom: 10px;
    }
  }
  


</style>