<template>
  <div class="div">
    <Navbar />
    <Header />
    <Testimonial />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Header from "./components/Header.vue";
import Testimonial from "./components/testimonial.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Header,
    Testimonial,
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  border: 0;
}

:root {
  --primary-color: #333;
  --secondary-color: rgb(185, 1, 1);
  --ternary-color: #f4f4f4;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100vw;
  height: 100vh;
}
</style>
