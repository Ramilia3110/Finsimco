<template>
  <div class="banner2">
    <div class="img-box">
      <img class="bg1" src="@/assets/banner2.png" alt />
    </div>
  </div>
</template>

<script>
export default {
  name: "Banner2"
};
</script>

<style lang="scss" scoped>
.banner2 {
  background: #01c9dc;

  height: 70vh;
}
.bg1 {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center center;
}
@media only screen and (max-width: 992px) {
  .banner2 {
    height: auto;
  }
}
</style>