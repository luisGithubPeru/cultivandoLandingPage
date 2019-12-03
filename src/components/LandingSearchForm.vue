<template>
  <div class="container">
    <form class="form-style" v-on:submit.prevent >
      <h2>Busca tu producto</h2>
      <ul class="grid">
        <li>
          <label for="name">Producto</label>
          <input class="input" type="text" name="name" maxlength="100" />
          <span>Nombre de Producto</span>
        </li>
        <li>
          <label for="type">Tipo</label>
          <select class="input" name="type">
            <option key="1" value="organico">Orgánico</option>
            <option key="2" value="tradicional">Tradicional</option>
          </select>
          <span>Producto Orgánico o Tradicional</span>
        </li>
        <li>
          <label for="price">Precio</label>
          <input class="input" type="text" name="price" maxlength="100" />
          <span>Precio del producto</span>
        </li>
        <li>
          <label for="stage">Etapa</label>
          <select class="input" name="stage">
            <option key="1" value="siembra">Siembra</option>
            <option key="2" value="cosecha">Cosecha</option>
          </select>
          <span>Etapa de Siembra o Cosecha</span>
        </li>
        <li>
          <label for="location">Departamento</label>
          <input class="input" type="text" name="location" />
          <span>Ubicación</span>
        </li>
      </ul>
      <input class="submit" type="submit" value="Buscar"  />
    </form>
    <LandingSearchResults v-bind:results="payload" />
  </div>
</template>


<style lang="scss" scoped>
.container {
  margin-bottom: 100px;
}
.grid {
  display: grid;
  margin: 0 50px;
}

@media only screen and (min-width: 950px) {
  .grid {
    grid-template-columns: repeat(5, 1fr);
    grid-gap: 2rem;
  }
}
@media only screen and (max-width: 950px) {
  .grid {
    grid-template-columns: 1fr;
  }
}

.form-style {
  margin: 130px 0px;
  & > ul {
    list-style: none;
    padding: 0;
    & > li {
      padding: 9px;
      border: 1px solid #dddddd;
      margin-bottom: 30px;
      border-radius: 3px;
      & > label {
        float: left;
        margin-top: -19px;
        background: #ffffff;
        padding: 2px 5px 2px 5px;
        color: #b9b9b9;
      }
      & > .input {
        width: 100%;
        border: none;
        line-height: 25px;
        padding: 0;
      }
      & > select {
        padding-left: 40% !important;
        height: 1.5rem;
      }
      & > span {
        background: #f3f3f3;
        display: block;
        padding: 3px;
        margin: 0 -9px -9px -9px;
        color: #c0c0c0;
        font-size: 11px;
      }
    }
  }
}

.submit {
  background: #2471ff;
  border: none;
  padding: 10px 20px 10px 20px;
  border-bottom: 3px solid #5994ff;
  border-radius: 3px;
  color: #d2e2ff;
  &:hover {
    background: #6b9fff;
    color: #fff;
  }
}
</style>
<script>
import LandingSearchResults from "./LandingSearchResults.vue";
export default {
  components: {
    LandingSearchResults
  },
  data() {
    return {
      payload: [
        {
          id: 1,
          name: "Pepe",
          type: "Organico",
          stage: "En Siembra",
          price: "S/ 5.00",
          cert: "Global GAP",
          location: "Cañete"
        },
        {
          id: 2,
          name: "Pepo",
          type: "Organico",
          stage: "En Siembra",
          price: "S/ 5.00",
          cert: "Global GAP",
          location: "Cañete"
        },
        {
          id: 3,
          name: "Pipo",
          type: "Organico",
          stage: "En Siembra",
          price: "S/ 5.00",
          cert: "Global GAP",
          location: "Cañete"
        }
      ]
    };
  }
};
</script>