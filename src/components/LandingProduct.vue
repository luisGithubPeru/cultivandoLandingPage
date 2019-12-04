<template>
  <div class="card">
    <h3>{{product.name}} ({{product.quantity}} toneladas)</h3>
    <img :src="product.img" alt="Avatar" />
    <p class="name">
      <span>Categoría :</span>
      <span>{{product.category}}</span>
    </p>
    <p class="type">
      <span>Tipo :</span>
      <span>{{product.type}}</span>
    </p>
    <p class="price">
      <span>Precio promedio:</span>
      <span>{{product.avg_price}}</span>
    </p>
    <p class="cert">
      <span>Certificados frecuentes:</span>
      <span>{{product.cert}}</span>
    </p>
  </div>
</template>
<style lang="scss" scoped>
.card {
  padding: 20px 60px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
  &:hover {
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
  }
  span:nth-child(1) {
    clear: both;
    float: left;
  }
  span:nth-child(2) {
    float: right;
  }
}
</style>
<script>
export default {
  props: ["product"]
};
</script>