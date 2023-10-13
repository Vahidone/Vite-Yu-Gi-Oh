

<script>

import axios from 'axios';
import { store } from "./data/store";
import Header from './components/Header.vue';
import Main from './components/Main.vue';




export default {
  name:'App',
  components: {
    Header,
    Main
  },
  data(){
    return{
      store
    }
  },
  methods:{
    getApi(){
      axios.get(store.apiUrl, {
        params: {
          name: store.nameToSearch,
          status: store.statusToSearch
        }

      })
        .then(result =>{

          console.log(result.data);
          store.cardList = result.data.data
        })
        .catch(error => {
          console.log(error);
        })
    }
  },
  mounted(){
    this.getApi();
    console.log(store.cardList);
  }
}
</script>


<template>
  <Header/>
  <Main/>
</template>



<style lang="scss">

@use './scss/main.scss';

</style>
