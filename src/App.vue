<script>
import { store } from './data/store';
import axios from 'axios';
import Header from './components/Header.vue';
import Main from "./components/main.vue";
import SearchBar from './components/partials/SearchBar.vue';
export default {
  name:'App',
  components: {
    Header,
    Main,
    SearchBar
  },
  data(){
    return{
      store
    }
  },
  methods:{
    getApi() {
      axios.get(store.apiUrl,{
        params:{
          archetype:store.research
        }
      })
        .then(result =>{
          store.cardList = result.data.data

        })
        .catch(error => {
          store.research = [],
          store.cardList = ''
        })
    },
    getApiType(){
      axios.get(store.typeUrl)
        .then(result =>{
          store.archetypeList = result.data

        })
  
        .catch(error => {
          console.log(error);
        })
    },
   
  },
  mounted(){
    this.getApi();
    this.getApiType();
  }
}
</script>


<template>
  <Header/>
  <SearchBar @startSearch="getApi" />
  <Main @changeResearch="getApi"/>
</template>



<style lang="scss">

@use './scss/main.scss';

</style>
