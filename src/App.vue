<template>
  <div id="app">
    <LandingSlider />
    <LandingTutorial />
    <LandingProducts v-bind:products="products" />
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
  },
  data() {
    const img_base_path = "./assets/img/";
    return {
      products: [
        {
          id: 1,
          name: "Palta",
          category: "Palta",
          type: "Organico",
          avg_price: "S/ 5.00 x kg",
          cert: "Global GAP, Senasa",
          quantity: "207",
          img: require(img_base_path + "palta.png")
        },
        {
          id: 2,
          name: "Arandano Biloxi",
          category: "Arandanos",
          type: "Organico",
          avg_price: "S/ 14.00 x kg",
          cert: "Global GAP",
          quantity: "100",
          img: require(img_base_path + "arandano.png")
        },
        {
          id: 3,
          name: "Tomate",
          category: "Tomates",
          type: "Organico",
          avg_price: "S/ 5.00 x kg",
          cert: "Global GAP",
          quantity: "311",
          img: require(img_base_path + "tomate.png")
        }
      ]
    };
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
