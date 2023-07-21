<script>
import axios from "axios";
import { store } from "../store";

export default {
  data() {
    return {
      store,
      arrCocktails: [],
    };
  },
  created() {
    axios.get(this.store.baseUrl + "api/cocktails/random").then((response) => {
      this.arrCocktails = response.data.results;
    });
  },
};
</script>

<template>
  <div class="row row-cols-3 g-0">
    <div class="col" v-for="cocktail in arrCocktails" :key="cocktail.id">
      <router-link
        class="d-block w-100 h-100"
        :to="{ name: 'cocktails.show', params: { cocktail: cocktail.id } }"
      >
        <img
          class="w-100 h-100"
          :src="cocktail.strDrinkThumb"
          :alt="cocktail.name"
        />
      </router-link>
    </div>
  </div>
</template>

<style scoped>
.row {
  height: 70vh;
  padding-top: 2rem;
}

.col {
  height: calc(100% / 3);
}

img {
  object-fit: cover;
}
</style>
