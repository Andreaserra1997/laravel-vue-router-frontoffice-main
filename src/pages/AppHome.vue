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
    axios.get("http://localhost:8000/api/cocktails/random").then((response) => {
      this.arrCocktails = response.data.results;
    });
  },
};
</script>

<template>
  <!-- <div class="row row-cols-3 g-0">
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
  </div> -->



  <!-- Jumbotron -->
  <div class="container-fluid p-5 text-center bg-image rounded-3" style="
    background-image: url('https://cutewallpaper.org/21x/efzi79fd6/Celebrate-diversity-Wallpaper-and-Background-Image-.jpg');
    height: 80vh;
  ">
    <div class="mask bg-dark">
      <div class="d-flex justify-content-center align-items-center">
        <div class="text-white m-5">
          <h1 class="mb-3">The Cocktail Bar</h1>
          <h4 class="mb-3">Find-out our drinks!</h4>
          <button class="button type1">
            <router-link :to="{ name: 'cocktails.index' }" class="nav-link text-dark">COCKTAILS</router-link> </button>




        </div>
      </div>
    </div>
  </div>
  <!-- Jumbotron -->
</template>

<style scoped>
/* .row {
  height: 70vh;
  padding-top: 2rem;
}

.col {
  height: calc(100% / 3);
} */
/* img {
  object-fit: cover;
} */

.button {
  height: 50px;
  width: 200px;
  position: relative;
  cursor: pointer;
  border: 2px solid;
  overflow: hidden;
  border-radius: 30px;
  transition: all 0.2s ease-in-out;
}



.btn-txt {
  z-index: 1;
  font-weight: 800;
  letter-spacing: 4px;
}

.type1::after {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  transition: all 0.2s ease-in-out;
  background-color: #333;
  border-radius: 30px;
  visibility: hidden;
  height: 10px;
  width: 10px;
  z-index: -1;
}

.button:hover {
  box-shadow: 1px 1px 200px #252525;
  color: #fff;
  border: none;
}

.type1:hover::after {
  visibility: visible;
  transform: scale(100) translateX(2px);
}
</style>
