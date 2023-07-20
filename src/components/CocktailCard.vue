<script>
import { store } from "../store";

export default {
  data() {
    return {
      store,
    };
  },
  props: {
    cocktail: {
      type: Object,
      required: true,
    },
  },
};
</script>

<template>
  <div class="card h-100">
    <img :src="cocktail.strDrinkThumb" class="card-img-top" />
    <div class="card-body">
      <h5 class="card-title">{{ cocktail.strDrink }}</h5>
    </div>
    <div class="card-body d-flex flex-column">
      <ul class="list-group list-group-flush">
        <li class="list-group-item">{{ cocktail.strAlcoholic }}</li>
        <li class="list-group-item">{{ cocktail.dateModified }}</li>
        <li class="list-group-item">{{ cocktail.strCategory }}</li>
      </ul>
    </div>
    <router-link
      :to="{ name: 'cocktails.show', params: { cocktail: cocktail.id } }"
      class="btn btn-primary mt-auto"
      >View</router-link
    >
  </div>
</template>

<style>
.card {
  margin: 1rem;
  height: 100%;
}
</style>
