<template>
  <div class="footer">
    <div>
      <router-link to="/">Home</router-link>|
      <router-link to="/careers">Careers</router-link>
      <router-link to="/privacy">Privacy</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  components: {}
};
</script>

<style lang="scss" scoped>
.footer {
  padding: 30px;
  background: #01c9dc;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>