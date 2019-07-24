<template>
  <table style="border:1px solid black">
    <tr>
      <th>Vintage</th>
      <th>Country</th>
      <th>County</th>
      <th>Designation</th>
      <th>Points</th>
      <th>Price</th>
      <th>Province</th>
      <th>Title</th>
      <th>Variety</th>
      <th>Winery</th>
    </tr>
    <td>{{vintage}}</td>
    <td>{{country}}</td>
    <td>{{county}}</td>
    <td>{{designation}}</td>
    <td>{{points}}</td>
    <td>{{price}}</td>
    <td>{{province}}</td>
    <td>{{title}}</td>
    <td>{{variety}}</td>
    <td>{{winery}}</td>
  </table>
</template>


<script>
export default {
  name: "WineVintage",
  props: {
    vintage: String,
    country: String,
    county: String,
    designation: String,
    points: String,
    price: String,
    province: String,
    title: String,
    variety: String,
    winery: String
  }
};
</script>

<style scoped>
h1 {
  font-weight: bolder;
}
</style>
