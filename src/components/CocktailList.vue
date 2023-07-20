<script>
import axios from "axios";
import CocktailCard from "./CocktailCard.vue";
import { store } from "../store";

export default {
  data() {
    return {
      store,
    };
  },
  components: {
    CocktailCard,
  },
  data() {
    return {
      arrCocktails: [],
    };
  },
  methods: {
    getCocktails() {
      axios.get("http://localhost:8000/api/cocktails").then((response) => {
        this.arrCocktails = response.data.results;
      });
    },
  },
  created() {
    this.getCocktails();
  },
};
</script>

<template>
  <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 g-4 mb-5">
    <div class="col" v-for="cocktail in arrCocktails" :key="cocktail.id">
      <CocktailCard :cocktail="cocktail" />
    </div>
  </div>
</template>

<style></style>
