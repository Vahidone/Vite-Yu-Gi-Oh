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
  <div class="col-csm">
    <div class="card-csm">
      <img :src="img">
      <h6>{{ name }}</h6>
      <p>{{ type }}</p>
    </div>
  </div>
</template>



<style lang="scss" scoped>
@use '../../../scss/partials/variables' as *;
@use '../../../scss/partials/general' as *;


.col-csm{
  width: 20%;
  margin-bottom: 15px;
}
.card-csm{
  background-color: $background-orange;
  text-align: center;
  height: $h-100;
  img{
    max-width: $max-100;
    margin-bottom: 10px;
    }
  }
  


</style>