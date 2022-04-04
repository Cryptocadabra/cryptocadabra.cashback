<template>
  <section class="hero" id="hero">
    <div class="hero__container container">
      <div class="hero__text text">
        <h1 class="hero__title">
          trading without cashback, you lose $30 on $100 in commissions paid
        </h1>
        <p class="hero__description">
          You can easily earn extra income from trading by getting commission
          rebates. We'll give you back up to $30 every time you pay $100 in
          commissions. Sounds good? Then keep reading.
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
  margin-top: 100px;
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
