<template>
  <!-- template syntax is {{prop being passed}} -->
  <div>
    <BottleWinery id="winery" v-bind:winery="winery">{{winery}}</BottleWinery>
    <h2>Title: {{title}}</h2>
  </div>
</template>

<script>
import BottleWinery from "./BottleWinery";
// name has to be the same as what you're using in other component, i think lel
// need to add props which are being used in this component
export default {
  name: "BottleTitle",
  props: {
    title: String,
    winery: String
  },
  components: {
    BottleWinery
  }
};
</script>


<style scoped>
/* scoped just means the styles apply to this component only */
#winery {
  margin: 0;
}
h2 {
  margin: 0;
}
</style>
