<template>
  <div class="grid">
    <div class="logo">
      <a href="http://cultivandoperu.com/" target="blank">
        <img src="../assets/img/logo.png" />
      </a>
    </div>
    <div class="slogan">
      <p>
        "Te ayudamos a encontrar los productos que
        <br />necesites."
      </p>
    </div>
    <div class="facebook">
      <a href="https://www.facebook.com/CultivandoNegocios/" target="blank">
        <img src="../assets/img/facebook.png" />
        <span>@CultivandoNegocios</span>
      </a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
/* All screen styles   */
a {
  color: #fff;
  text-shadow: 5px 5px 25px;
}

.grid {
  display: grid;
  background-image: url(../assets/img/slider1.png);

  .slogan {
    font-size: 1.5rem;
    color: #fff;
  }

  .facebook {
    img {
      vertical-align: middle;
    }
    span {
      margin-left: 10px;
    }
  }
}

/* PC screen */
@media only screen and (min-width: 772px) {
  .grid {
    grid-template-columns: 1fr 2fr;

    .logo {
      justify-self: start;
    }

    .slogan {
      justify-self: start;
      align-self: end;
    }

    .facebook {
      grid-column: 2;
      justify-self: end;
      align-self: center;
      padding-right: 100px;
      padding-bottom: 20px;
    }
  }
}

/* Tablet screen */
@media only screen and (max-width: 772px) {
  .grid {
    .logo {
      justify-self: center;
      img {
        width: 8rem;
      }
    }
    .slogan {
      justify-self: center;
      padding-bottom: 1rem;
    }
    .facebook {
      padding-bottom: 10px;
      font-size: 0.9rem;
      img {
        width: 2rem;
      }
    }
  }
}
</style>
