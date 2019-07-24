<template>
  <div>
    <h3>Country: {{country}}| County: {{county}}| Province: {{province}}</h3>
  </div>
</template>

<script>
export default {
  name: "BottleGeography",
  props: {
    country: String,
    county: String,
    province: String
  }
};
</script>

<style scoped>
h3 {
  margin: 0;
}
</style>
