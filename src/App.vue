<script>
import CharacterCard from "./components/CharacterCard.vue";
import CardsContainer from "./components/CardsContainer.vue";

export default {
  name: "App",
  components: {
    CardsContainer,
    CharacterCard,
  },
};
</script>

<template>
  <h1>sono App</h1>
</template>

<style lang="scss">
@use "./scss/main.scss";
@import "bootstrap/scss/bootstrap";
</style>
