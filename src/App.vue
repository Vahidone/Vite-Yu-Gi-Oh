<script>
import {store} from "./data/store";
import CharacterCard from "./components/CharacterCard.vue";
import CardsContainer from "./components/CardsContainer.vue";
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";

export default {
  name: "App",
  data () {
    return {
      store
    }
  },
  
 
  components: {
    CardsContainer,
    CharacterCard,
    Header,
    Main,
    
    
   
  },
};
</script>

<template>
  <Header />
  <Main />
  <CardsContainer />
  <CharacterCard />
</template>

<style lang="scss">
@use "./components/scss/main.scss";

</style>
