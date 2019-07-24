<template>
  <div id="bottleLayout">
    <BottleTitle v-bind:winery="winery" v-bind:title="title" id="BottleTitle"></BottleTitle>
    <BottleGeography
      v-bind:country="country"
      v-bind:county="county"
      v-bind:province="province"
      id="BottleGeography"
    ></BottleGeography>
    <BottleVariety v-bind:variety="variety" id="BottleVariety"></BottleVariety>
    <BottlePrice v-bind:price="price" v-bind:points="points" id="BottlePrice"></BottlePrice>
  </div>
</template>


<script>
import BottleVintage from "./BottleVintage";
import BottleGeography from "./BottleGeography";
import BottleDesignation from "./BottleDesignation";

import BottlePoints from "./BottlePoints";
import BottlePrice from "./BottlePrice";
import BottleTitle from "./BottleTitle";

import BottleVariety from "./BottleVariety";
import BottleWinery from "./BottleWinery";

export default {
  name: "WineBottle",
  props: {
    vintage: String,
    country: String,
    county: String,
    designation: String,
    points: Number,
    price: String,
    province: String,
    title: String,
    variety: String,
    winery: String
  },
  components: {
    BottleTitle,
    BottleGeography,
    BottleDesignation,
    BottlePoints,
    BottlePrice,
    BottleVariety,
    BottleWinery
  }
};
</script>

<style>
#bottleLayout {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(2, 1fr);
  height: 100%;
  width: 60%;
  background-color: #3333;
  margin: 0;
  margin-bottom: 5%;
  padding: 2%;

  margin: auto;
  margin-bottom: 5%;
  border-radius: 10px;
}

#BottleTitle,
#BottleGeography,
#BottleVariety {
  grid-column: 1/5;
  text-align: left;
  margin: 0;
}
#BottleTitle h3,
#BottleGeography h3,
#BottleVariety h3 {
  font-weight: 100;
  margin: 0;
}

#BottlePrice,
#BottlePoints {
  grid-column: 4/5;
  text-align: right;
}
</style>
