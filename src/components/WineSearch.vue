<template>
  <div>
    <input v-model="search" placeholder="Search for a wine" />

    <div v-if="search">
      <div v-for="wine in filteredWines" v-bind:key="wine.Title">
        <!-- <h1>{{wine.Title}}</h1> -->
        <WineBottle
          v-bind:vintage="wine.Vintage"
          v-bind:country="wine.Country"
          v-bind:county="wine.County"
          v-bind:designation="wine.Designation"
          v-bind:points="wine.Points"
          v-bind:price="wine.Price"
          v-bind:province="wine.Province"
          v-bind:title="wine.Title"
          v-bind:variety="wine.Variety"
          v-bind:winery="wine.Winery"
        />
      </div>
    </div>

    <div v-else>
      <h1>Search something..</h1>
    </div>
  </div>
</template>

<script>
import WineBottle from "./WineBottle";
export default {
  name: "WineSearch",
  props: { search: String, wines: [] },
  components: { WineBottle },

  computed: {
    filteredWines: function() {
      return this.wines.filter(wine => {
        return wine.Title.toLowerCase().match(this.search.toLowerCase());
      });
    }
  }
};
</script>

<style>
</style>
