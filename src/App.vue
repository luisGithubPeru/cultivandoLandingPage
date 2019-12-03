<template>
  <div id="app">
    <LandingSlider />
    <LandingTutorial />
    <LandingProducts />
    <LandingSearchForm />
  </div>
</template>

<script>
import LandingSlider from "./components/LandingSlider.vue";
import LandingTutorial from "./components/LandingTutorial.vue";
import LandingProducts from "./components/LandingProducts.vue";
import LandingSearchForm from "./components/LandingSearchForm.vue";

export default {
  name: "app",
  components: {
    LandingSlider,
    LandingTutorial,
    LandingProducts,
    LandingSearchForm
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0px;
}
</style>
