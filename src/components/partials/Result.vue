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
      return 'Cards no found';
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
  width: $w-100;
  color: white;
  background-color:$background-result ;
  padding: 10px;
}

</style>