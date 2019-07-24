<template>
  <div>
    <h3>Variety: {{variety}}</h3>
  </div>
</template>

<script>
export default {
  name: "BottleVariety",
  props: {
    variety: String
  }
};
</script>
  
<style>
h3 {
  font-weight: 100;
  margin: 0;
}
</style>
