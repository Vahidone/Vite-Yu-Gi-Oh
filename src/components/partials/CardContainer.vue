<script>
import { store } from '../../data/store';
import Cards from './Cards.vue';
import Result from './Result.vue';
export default {
  name:'CardContainer',
  components:{
    Cards,
    Result
  },
  data(){
    return{
      store
    }
  },
  mounted(){
    console.log(store.cardList);
  }
}
</script>


<template>
  <div class="container mt-5">
    <Result/>     
    <div class="row">
      <Cards
      v-for="card in store.cardList"
      :key ="card.id"
      :img = "card.card_images[0].image_url"
      :name = "card.name"
      :type = "card.archetype"

      />
    </div>

  </div>
</template>



<style lang="scss" scoped>
@use "../../../scss/partials/variables" as *;

  .container {
    background-color: $bg-white;
    padding: 45px 35px 0 35px;
  }

</style>