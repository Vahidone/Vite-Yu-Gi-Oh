

<script>
import { store } from "../../data/store";

export default {
  name: 'SearchBar',
  data () {
    return {
      store
    }
  },
  methods: {
    reset () {
      store.research = '',
      this.$emit('startSearch'),
      this.store.cardList = ''
    }
  }
}
</script>


<template>
  <div class="container-csm">
    <div class="row">
      <div class="col-auto">
        <input v-model="store.research" type="text" class="form-control" placeholder="Search Archetype">
      </div>
      <div class="col-auto">
        <button @click="$emit('startSearch')" class="btn btn-info">Search</button>
      </div>
      <div class="col-auto">
        <button @click="reset" class="btn btn-danger">Reset</button>
      </div>
    </div>
  </div>
  
</template>


<style lang="scss" scoped>
.container-csm {
  display: flex;
  justify-content: end;
  padding-right: 300px
}
 
</style>