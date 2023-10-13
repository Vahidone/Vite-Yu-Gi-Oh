

<script>
import { store } from '../../data/store';

export default {
  name: 'SearchBar',
  data () {
    return {
      store
    }
  },
  methods: {
    reset () {
      store.nameToSearch = '',
      store.statusToSearch = '',
      $emit('startSearch')
    }
  }

}
</script>

<template>
  <div class="container-csm">
    <div class="row justify-content-center">
      <div class="col-auto">
        <input v-model="store.nameToSearch" type="text" class="form-control" placeholder="Search Character">
      </div>
      <div class="col-auto">
        <select class="form-select" aria-label="Default select example">
          <option selected>Select status</option>
          <option value="alive">Alive</option>
          <option value="dead">Dead</option>
          <option value="unknown">Unknown</option>
        </select>
      </div>
      <div class="col-auto">
        <button @click="$emit('startSearch')" class="btn btn-info">Search</button>
      </div>
      <div class="col-auto">
        <button @click="reset" class="btn btn-warning">Reset</button>
      </div>

    </div>
  </div>
</template>

<style lang="scss" scoped>

</style>