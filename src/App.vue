<template>
  <div id="app">
    <Nav />
    <router-view />
    <Footer />
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";
import Footer from "@/components/Footer.vue";
export default {
  name: "App",
  components: {
    Nav,
    Footer
  }
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Barlow:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600&display=swap");
$color-primary: #01c9dc;
*,
*::before,
*::after {
  box-sizing: inherit;
  margin: 0;
  padding: 0;
  font-family: "Barlow", sans-serif;
}
html {
  font-size: 62.5%;
  scroll-behavior: smooth;
}
body {
  box-sizing: border-box;
  background-color: #fff;
  width: 100%;
  height: 100%;
}
</style>