<template>
  <section class="hero" id="tracker">
    <div class="hero__container container">
      <div class="hero__text text">
        <h1 class="hero__title">
          Want to keep track of how much cashback you've earned?
        </h1>
        <p class="hero__description">
          We created a special Telegram bot that can track the amount of
          cashback you've earned. If you are a member of our project, tell the
          bot your ID and you will be given a statement.
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
