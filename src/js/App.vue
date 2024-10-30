<template>
  <div>
    <Nav @menu-toggle="handleMenuToggle" />
    <Header :isMenuOpen="isMenuOpen" />
    <Articles :isMenuOpen="isMenuOpen" />
    <Programming :isMenuOpen="isMenuOpen" />
    <Ended :isMenuOpen="isMenuOpen" />
    <ScrollToTop />
  </div>
</template>

<script>
import Nav from "./components/Nav.vue";
import Header from "./components/Header.vue";
import Articles from "./components/Articles.vue";
import Programming from "./components/Programming.vue";
import Ended from "./components/Ended.vue";
import ScrollToTop from "./components/ScrollToTop.vue";

export default {
  components: { Nav, Header, Articles, Programming, Ended, ScrollToTop },
  data() {
    return {
      isMenuOpen: false,
    };
  },
  methods: {
    handleMenuToggle(isOpen) {
      this.isMenuOpen = isOpen;
    },
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Raleway:ital,wght@0,100..900;1,100..900&display=swap");
$mainTextColor: #ababab;
$commonColor: #19ddff;
* {
  margin: 0;
  padding: 0;
}

body {
  background-color: #fff;
  color: #000000;
  font-family: "Poppins", sans-serif;
  font-weight: 400;
  font-size: 1em;
}

a {
  text-decoration: none;
}

.container {
  @media (min-width: 1500px) {
    width: 1300px;
    margin: 0 auto;
  }
  @media (max-width: 1500px) and (min-width: 900px) {
    width: 80%;
    margin: 0 10%;
  }
  @media (max-width: 900px) {
    width: 90%;
    margin: 0 5%;
  }
}
</style>
