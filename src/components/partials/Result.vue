<script>
import { store } from '../../data/store';
export default {
  name:'Result',
  data(){
    return{
      store
    }
  },
  computed:{
    outputResult(){
      if(store.cardList.length > 0){
        return 'Found ' + store.cardList.length + ' cards';
      }
      return 'Cards not found';
    }
  }
}
</script>


<template>
  <div class="result">
    <span>{{ outputResult }}</span>
  </div>
</template>



<style lang="scss" scoped>
@use '../../../scss/partials/variables' as *;

.result {
  width: 100%;
  color: $color-white;
  background-color:$bg-result ;
  padding: 10px;
}

</style>