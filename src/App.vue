<template>
  <div id="app">
    <!-- use components as html tags, each component must return 1 html element,
    template doesnt count. I just threw everything into a <div>
      v-bind:<prop name>=<value>
    v-bind is vues way to pass properties(props)
    props are just attributes, so you can use them in the components-->
    <WineSearch v-bind:wines="myBottles"></WineSearch>
    <!-- <WineBottle
      v-bind:vintage="myBottles[0].Vintage"
      v-bind:country="myBottles[0].Country"
      v-bind:county="myBottles[0].County"
      v-bind:designation="myBottles[0].Designation"
      v-bind:points="myBottles[0].Points"
      v-bind:price="myBottles[0].Price"
      v-bind:province="myBottles[0].Province"
      v-bind:title="myBottles[0].Title"
      v-bind:variety="myBottles[0].Variety"
      v-bind:winery="myBottles[0].Winery"
    />-->
  </div>
</template>

<script>
// WineBottle is a component,it has a bunch of other components and styles
import WineBottle from "./components/WineBottle.vue";
import WineSearch from "./components/WineSearch.vue";

import json from "./assets/csvjson.json";

// name = name of component being exported
// components = components being used in component
// data = data being used, pulled from json file
export default {
  name: "app",
  components: {
    WineBottle: WineBottle,
    WineSearch
  },
  data() {
    return {
      myBottles: json
    };
  }
};
</script>

<style>
body,
html {
  width: 100%;
  height: 100%;
  margin: 0;
  overflow-x: hidden;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  margin: 0;
  width: 100%;
}
#layout {
  display: grid;
  /* grid-template-column creates 3 equal columns */
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 1fr);
  width: 100%;
}
</style>
