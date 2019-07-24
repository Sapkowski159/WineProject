<template>
  <div>
    <BottlePoints v-bind:points="points"></BottlePoints>
    <h1>Price: {{price}}</h1>
  </div>
</template>

<script>
import BottlePoints from "./BottlePoints";
export default {
  name: "BottlePrice",
  props: {
    price: String,
    points: Number
  },
  components: {
    BottlePoints
  }
};
</script>

<style>
</style>
