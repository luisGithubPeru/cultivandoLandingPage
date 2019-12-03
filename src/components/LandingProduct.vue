<template>
  <div class="card">
    <h3>PALTA HASS</h3>
    <img src="../assets/img/palta.png" alt="Avatar" />
    <p class="name">
      <span>Productor :</span>
      <span>{{name}}</span>
    </p>
    <p class="type">
      <span>Tipo :</span>
      <span>{{type}}</span>
    </p>
    <p class="stage">
      <span>Etapa de Producción:</span>
      <span>{{stage}}</span>
    </p>
    <p class="price">
      <span>Precio:</span>
      <span>{{price}}</span>
    </p>
    <p class="cert">
      <span>Certificados:</span>
      <span>{{cert}}</span>
    </p>
    <p class="location">
      <span>Ubicación:</span>
      <span>{{location}}</span>
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
  props: {
    name: { type: String, default: "Roberto Perez" },
    type: { type: String, default: "Organico" },
    stage: { type: String, default: "En Siembra" },
    price: { type: String, default: "S/ 5.00" },
    cert: { type: String, default: "Global GAP" },
    location: { type: String, default: "Cañete" }
  }
};
</script>