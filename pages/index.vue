<template>
  <div>
    <Hero />
    <About />
    <section class="works">
      <h1>Works</h1>
    </section>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Hero from "@/components/Hero.vue";
import About from "@/components/About.vue";

export default Vue.extend({
  name: "IndexPage",
  components: {
    Hero,
    About,
  },
});
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Roboto+Mono:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&display=swap");
@import "~/assets/scss/main.scss";

body {
  background-color: $color-bg-theme;
  font-family: "Roboto Mono", monospace;
  padding: 0px 150px;
  color: #e6f1ff;
}

@media screen and (max-width: 1080px) {
  body {
    padding: 0px 50px;
  }
}
@media screen and (max-width: 768px) {
  body {
    padding: 0px 30px;
  }
}
</style>

<style>
section {
  max-width: 900px;
  margin: 0 auto;
}
</style>
