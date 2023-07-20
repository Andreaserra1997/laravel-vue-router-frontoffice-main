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
      arrCategories: [],
    };
  },
  methods: {
    getCocktails() {
      axios.get("http://localhost:8000/api/cocktails").then((response) => {
        this.arrCocktails = response.data.results;
      });
    },
    getCategories() {
      axios.get("http://localhost:8000/api/categories").then((response) => {
        this.arrCategories = response.data.results;
      });
    },
  },
  created() {
    this.getCocktails();
    this.getCategories();
  },
};
</script>

<template>
  <form>
    <h2>Filtra le Categorie</h2>

    <label for="categories">Categorie</label>
    <select class="form-select" id="categories">
      <option
        v-for="category in arrCocktails"
        :key="category.id"
        :value="category.id"
      >
        {{ category.strCategory }}
      </option>
    </select>
  </form>

  <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 g-4 mb-5">
    <div class="col" v-for="cocktail in arrCocktails" :key="cocktail.id">
      <CocktailCard :cocktail="cocktail" />
    </div>
  </div>
</template>

<style></style>
