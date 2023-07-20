<script>
import axios from "axios";
import { store } from "../store";
import page404 from "./page404.vue";

export default {
  components: {
    page404,
  },
  data() {
    return {
      cocktail: null,
      store,
      is404: false,
    };
  },
  created() {
    axios
      .get("http://localhost:8000/api/cocktails/" + this.$route.params.cocktail)
      .then((response) => {
        if (response.data.success) {
          this.cocktail = response.data.results;
        } else {
          // this.$router.push({ name: "page404" });
          this.is404 = true;
        }
      });
  },
};
</script>

<template>
  <page404 v-if="is404" />
  <template v-if="cocktail">
    <h1>{{ cocktail.strDrink }}</h1>
    <img :src="cocktail.strDrinkThumb" :alt="cocktail.strDrink" />
    <p>{{ cocktail.strInstructionsIT }}</p>
  </template>
</template>

<style></style>
