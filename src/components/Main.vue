


<script>
import CardContainer from './partials/CardContainer.vue';
import SearchBar from './partials/SearchBar.vue';
export default {
  name:'Main',
  components:{
    CardContainer,
    SearchBar
  }
}
</script>


<template>
  <main>
    <SearchBar />
    <CardContainer/>
   
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