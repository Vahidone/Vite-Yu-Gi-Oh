

<script>
import { store } from '../../data/store';
export default {
  name: 'SearchBar',
  data(){
    return{
      store
    }
  }

}
</script>
<template>
  <div class="container-csm">
    <div class="row">
      <div class="col-auto">
        <input type="text" class="form-control" placeholder="Search Character">
      </div>
      <div class="col-auto">
        <button class="btn btn-info">Search</button>
      </div>
      <div class="col-auto">
        <button class="btn btn-danger">Reset</button>
      </div>
    </div>
  </div>
  
</template>

<style lang="scss" scoped>
.container-csm {
  padding-left: 87px;
}
 
</style>