<template>
  <div>
    <h1>Resultados de tu búsqueda</h1><br />
    <div class="grid grid-header">
      <span>Productor</span>
      <span>Tipo</span>
      <span>Etapa de Producción</span>
      <span>Precio</span>
      <span>Certificados</span>
      <span>Ubicación</span>
    </div>
    <div class="grid" v-bind:key="result.id" v-for="result in results">
      <div>{{ result.name }}</div>
      <div>{{ result.type }}</div>
      <div>{{ result.stage }}</div>
      <div>{{ result.price }}</div>
      <div>{{ result.cert }}</div>
      <div>{{ result.location }}</div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.grid {
  max-width: 1000px;
  margin: auto;
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  grid-gap: 2em;
  color: #222;
  border-bottom: 1px solid #ddd;
  padding: 1em 0;
  span {
    font-weight: bold;
  }
}

@media (max-width: 600px) {
  .grid {
    grid-template-columns: 1fr;
    grid-gap: 0.5em;
  }

  .grid-header {
    display: none;
  }
}
</style>
<script>
export default {
  props: ["results"]
};
</script>