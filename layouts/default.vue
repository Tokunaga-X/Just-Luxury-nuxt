<template>
  <div class="app">
    <Loading v-if="loading" />
    <Nav />
    <nuxt />
    <Footer />
  </div>
</template>
<script>
import Nav from "./partials/Nav";
import Footer from "./partials/Footer";
import Loading from "../components/Loading";

export default {
  components: {
    Nav,
    Footer,
    Loading
  },
  data() {
    return {
      loading: true
    };
  },
  beforeCreate() {
    setTimeout(() => {
      this.loading = false;
    }, 1500);
  }
};
</script>
<style>
@import "https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.2/animate.min.css";

html {
  font-size: 16px;
  word-spacing: 1px;
  font-display: swap;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}
.app {
  width: 100%;
  min-height: 100%;
}
</style>
