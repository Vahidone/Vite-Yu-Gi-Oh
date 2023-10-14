<script>
import { store } from '../data/store';
import CardContainer from './partials/CardContainer.vue';
import SearchBar from './partials/SearchBar.vue';

export default {
  name:'Main',
  components:{
    CardContainer,
    SearchBar
  },
  data(){
    return{
      store
    }
  }
}
</script>


<template>
  <main>
    <div class="container-csm">
      <select 
          @change="$emit('changeResearch')" 
          v-model="store.research"
          class="form-select form-select-sm" 
          aria-label="Small select example">
          <option  selected value="">Select Archtype</option>
          <option
            v-for="(arch, index) in store.archetypeList"
            :key="index"
            :value="arch.archetype_name"
            >{{ arch.archetype_name }}

          </option>
        </select>
      <SearchBar />
      <CardContainer/>
    </div>
  </main>
</template>



<style lang="scss" scoped>
@use '../../scss/partials/variables' as *;

  main {
    background-color: $bg-orange;
    padding-top: 20px;
    select {
      width: 160px;
      height: 40px;
      margin-left: 170px;
      margin-bottom: 20px;
    }
   
  }
</style>