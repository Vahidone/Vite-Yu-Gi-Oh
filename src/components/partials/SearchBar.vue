

<script>
export default {
  name: 'SearchBar'

}
</script>

<template>
  <div class="container-csm">
    <div class="row justify-content-center">
      <div class="col-auto">
        <input type="text" class="form-control" placeholder="Search Character">
      </div>
      <div class="col-auto">
        <select class="form-select" aria-label="Default select example">
          <option selected>Select status</option>
          <option value="1">Alive</option>
          <option value="2">Dead</option>
          <option value="3">Unknown</option>
        </select>
      </div>
      <div class="col-auto">
        <button class="btn btn-info">Search</button>
      </div>
      <div class="col-auto">
        <button class="btn btn-warning">Reset</button>
      </div>

    </div>
  </div>
</template>

<style lang="scss" scoped>

</style>