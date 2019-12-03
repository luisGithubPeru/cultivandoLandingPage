<template>
  <div class="container">
    <LandingProduct />
    <LandingProduct />
    <LandingProduct />
    <!-- <LandingProduct />
    <LandingProduct />
    <LandingProduct />-->
  </div>
</template>
<script>
import LandingProduct from "./LandingProduct.vue";
export default {
  components: {
    LandingProduct
  }
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