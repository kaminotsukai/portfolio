<template>
  <div>
    <BaseSection>
      <About />
    </BaseSection>
    <!-- <Hero /> -->
    <BaseSection title="Experience...">
      <Experience />
    </BaseSection>
    <!-- <Work /> -->
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import BaseSection from "@/components/BaseSection.vue";
import Hero from "@/components/Hero.vue";
import About from "@/components/About.vue";
import Work from "@/components/Work.vue";
import Experience from "@/components/Experience.vue";

export default Vue.extend({
  name: "IndexPage",
  components: {
    BaseSection,
    Hero,
    About,
    Work,
    Experience,
  },
});
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Roboto+Mono:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&family=Murecho:wght@100;200;300;400;500;600;700;800;900&display=swap");
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
