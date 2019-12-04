<template>
  <div>
    <h1>Productos más vendidos (por toneladas)</h1>
    <div class="container">
      <LandingProduct v-bind:product="products[0]" />
      <LandingProduct v-bind:product="products[1]" />
      <LandingProduct v-bind:product="products[2]" />
    </div>
  </div>
</template>
<script>
import LandingProduct from "./LandingProduct.vue";
export default {
  components: {
    LandingProduct
  },
  props:["products"]
};
</script>
<style lang="scss" scoped>
.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  grid-gap: 3em;
  padding: 0px 100px;
  margin: 0 0 50px 0;
}
</style>