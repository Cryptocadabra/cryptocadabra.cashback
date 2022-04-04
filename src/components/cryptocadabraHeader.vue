<template>
  <button @click="showMenu()" v-if="!isMenu" class="burger-button">
    <span class="burger-button__item"></span>
  </button>
  <button @click="closeBtn()" v-if="isMenu" class="close-button">
    <span class="close-button__item"></span>
  </button>
  <div v-if="isMenu" class="responsive-menu">
    <nav class="responsive-menu__nav nav">
      <ul class="nav-list responsive-menu__list">
        <li class="nav-list__item responsive-menu__item">
          <a href="#how-it-works" class="nav-list__link">How it works</a>
        </li>
        <li class="nav-list__item responsive-menu__item">
          <a href="#hero-instruction" class="nav-list__link">instruction</a>
        </li>
        <li class="nav-list__item responsive-menu__item">
          <a href="#rates" class="nav-list__link">brokers / markets</a>
        </li>
        <li class="nav-list__item responsive-menu__item">
          <a href="#tracker" class="nav-list__link">profit tracker</a>
        </li>
        <li class="nav-list__item responsive-menu__item">
          <a href="#faq" class="nav-list__link">faq</a>
        </li>
      </ul>
    </nav>
  </div>
  <header class="header">
    <!-- <div class="logo logo__container">
      <div class="logo__item">Cryptocadabra<span>.cashback</span></div>
    </div> -->
    <div class="header__container container">
      <nav class="header__nav nav">
        <ul class="nav-list">
          <li class="nav-list__item">
            <a href="#how-it-works" class="nav-list__link">How it works</a>
          </li>
          <li class="nav-list__item">
            <a href="#hero-instruction" class="nav-list__link">instruction</a>
          </li>
          <li class="nav-list__item">
            <a href="#rates" class="nav-list__link">brokers / markets</a>
          </li>
          <li class="nav-list__item">
            <a href="#tracker" class="nav-list__link">profit tracker</a>
          </li>
          <li class="nav-list__item">
            <a href="#faq" class="nav-list__link">faq</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isMenu: null,
    };
  },
  methods: {
    showMenu() {
      if (this.isMenu) {
        this.isMenu = false;
      } else {
        this.isMenu = true;
      }
    },
    closeBtn() {
      if (this.isMenu) {
        this.isMenu = false;
      } else {
        this.isMenu = true;
      }
    },
  },
};
</script>

<style>
/* Reset styles */
* {
  box-sizing: border-box;
}

:before,
:after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

a {
  text-decoration: none;
  color: inherit;
}

ul {
  padding: 0;
  list-style-type: none;
}

li {
  padding: 0;
}

span {
  color: #c58fff;
}

body {
  overflow-x: hidden;
}

.responsive-menu {
  margin: 0;
  padding-left: 10px;
  background: #212121;
  position: fixed;
  left: 0;
  top: 0;
  z-index: 999999;
  height: 1000vh;
  width: 50%;
}

.responsive-menu__list {
  align-items: baseline !important;
}

.burger-button {
  display: none;
  position: absolute;
  width: 45px;
  height: 45px;
  top: 15px;
  left: 5%;
  background: black;
  background: none;
  border: none;
  padding: 5px;
  margin: 0;
  z-index: 9999;
}

.close-button {
  position: fixed;
  width: 45px;
  height: 45px;
  top: 15px;
  left: 47%;
  background: black;
  background: none;
  border: none;
  padding: 5px;
  margin: 0;
  z-index: 9999;
  cursor: pointer;
}

.close-button__item {
  display: inline-block;
  vertical-align: middle;
  position: relative;
  border-radius: 4px;
  width: 70%;
  height: 3px;
  transform: rotate(45deg);
  background-color: white;
}

.close-button__item::after {
  content: "";
  display: inline-block;
  vertical-align: middle;
  position: relative;
  border-radius: 4px;
  width: 100%;
  bottom: 290%;
  height: 3px;
  transform: rotate(-90deg);
  background-color: white;
}

.burger-button:hover {
  background: #212121;
  cursor: pointer;
}

.burger-button__item {
  display: inline-block;
  vertical-align: middle;
  position: relative;
  border-radius: 4px;
  width: 70%;
  height: 3px;
  background-color: white;
}

.burger-button__item::before {
  content: "";
  position: absolute;
  width: 100%;
  border-radius: 4px;
  height: 3px;
  top: -8px;
  right: 0;
  background-color: #fff;
}

.burger-button__item::after {
  content: "";
  position: absolute;
  width: 100%;
  border-radius: 4px;
  height: 3px;
  bottom: -8px;
  right: 0;
  background-color: #fff;
}

.responsive-menu__list {
  display: flex;
  flex-direction: column;
}

.responsive-menu__item {
  margin-bottom: 15px;
}

.responsive-menu__item:hover {
  background: #000;
}

.container {
  width: 66.5625rem;
  margin: 0 auto;
}

.logo__container {
  width: 66.5625rem;
  margin: 0 auto;
  align-items: center;
}

.logo__item {
  font-size: 30px;
  text-align: center;
  font-weight: bold;
  text-transform: uppercase;
}

.header {
  padding-top: 30px;
  position: relative;
  left: 0;
  top: 0;
  width: 100%;
  font-size: 20px;
}

.header__container {
  display: block;
  padding: 0 20px;
  width: 66.5625rem;
  margin: 0 auto;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.nav-list {
  display: flex;
  font-size: 23px;
  align-items: center;
  font-weight: bold;
  text-transform: uppercase;
}

.nav-list__link {
  padding: 5px;
}

.nav-list__link:hover {
  background-color: #212121;
  color: #dcff02;
  transition: 0.2s;
}

.nav-list__item:not(:last-child) {
  margin-right: 40px;
}

/* Responsive starts here */
</style>
