<template>
  <button v-if="isVisible" @click="scrollToTop" class="scroll-to-top">
    <i class="fa-solid fa-arrow-up"></i> Наверх
  </button>
</template>
<script>
export default {
  data() {
    return {
      isVisible: false,
    };
  },
  methods: {
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: "smooth" });
    },
    handleScroll() {
      const headerHeight = document.querySelector(".main-div").offsetHeight;
      this.isVisible = window.scrollY > headerHeight;
    },
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>
<style lang="scss" scoped>
.scroll-to-top {
  position: fixed;
  bottom: 20px;
  right: 20px;
  padding: 10px;
  background-color: #8ab4f8;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 1.2em;
  opacity: 0.8;
  transition: transform 0.3s;
}

.scroll-to-top:hover {
  transform: scale(1.1);
  opacity: 1;
}
</style>
