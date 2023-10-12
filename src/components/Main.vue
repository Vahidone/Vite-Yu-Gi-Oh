


<script>
import CardContainer from './partials/CardContainer.vue';
export default {
  name:'Main',
  components:{
    CardContainer
  }
}
</script>


<template>
  <main>
    <div class="container-csm">
      <select class="form-select form-select-sm mt-4" aria-label="Small select example">
        <option selected>Alien</option>
        <option value="1">One</option>
        <option value="2">Two</option>
        <option value="3">Three</option>
      </select>
      <CardContainer/>
    </div>
  </main>
</template>



<style lang="scss" scoped>
@use '../../scss/partials/variables' as *;

  main {
    background-color: $background-orange;
    padding-top: 20px;
    select {
      font-size: 22px;
      width: 200px;
      height: 40px;
      margin-left: 185px;
    }
  }
</style>