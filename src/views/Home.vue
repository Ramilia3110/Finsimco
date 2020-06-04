<template>
  <div class="home">
    <Hero />
    <About id="about" />
    <Banner1 />
    <WhyUs id="why-with-us" />
    <Team id="team" />
    <Banner2 />
    <Contact id="contact" />
  </div>
</template>

<script>
import Hero from "@/components/Hero.vue";
import About from "@/components/Home/About.vue";
import Contact from "@/components/Home/Contact.vue";
import WhyUs from "@/components/Home/WhyUs.vue";
import Banner1 from "@/components/Home/Banner1.vue";
import Banner2 from "@/components/Home/Banner2.vue";
import Team from "@/components/Home/Team.vue";
export default {
  name: "Home",
  components: {
    Hero,
    About,
    Contact,
    WhyUs,
    Banner1,
    Banner2,
    Team
  }
};
</script>
<style lang="scss">
.home {
  margin: 0;
  padding: 0;
}
</style>