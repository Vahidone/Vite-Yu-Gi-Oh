<script>
import { store } from './data/store';
import axios from 'axios';
import Header from './components/Header.vue';
import Main from "./components/main.vue";
import SearchBar from './components/partials/SearchBar.vue';
import Loader from './components/partials/Loader.vue';

export default {
  name:'App',
  components: {
    Header,
    Main,
    SearchBar,
    Loader
  },
  data(){
    return{
      store
    }
  },
  methods:{
    getApi() {
      store.isLoading = true;
      axios.get(store.apiUrl,{
        params:{
          archetype:store.research
        }
      })
        .then(result =>{
          store.cardList = result.data.data
          store.isLoading = false;

        })
        .catch(error => {
          store.isLoading = false;
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
  <Loader v-if="store.isLoading" title="Loading..."/>
  <Main v-else @changeResearch="getApi"/>
</template>



<style lang="scss">

@use './scss/main.scss';

</style>
