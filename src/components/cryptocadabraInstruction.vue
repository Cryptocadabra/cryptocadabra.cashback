<template>
  <section class="hero" id="hero-instruction">
    <div class="hero__container container">
      <div class="hero__text text">
        <h1 class="hero__title">Want to join and get cashback with us?</h1>
        <p class="hero__description">
          Then follow this link and follow the clear instructions. If you have
          any difficulties, please contact our technical support.
        </p>
      </div>
      <div class="hero__img img">
        <img class="img__cryptocadabra" src="../assets/moneyRain.gif" alt="" />
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.hero {
  margin-top: 150px;
  margin-bottom: 100px;
}

.hero__container {
  display: flex;
  align-items: center;
  padding: 0 20px;
  width: 66.5625rem;
  max-width: 100%;
}

.hero__title {
  font-size: 45px;
  text-transform: uppercase;
  margin-bottom: 35px;
}

.hero__description {
  font-size: 20px;
}
</style>
