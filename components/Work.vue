<template>
  <section class="section-work">
    <h1 class="section-title">Works</h1>
  </section>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "Hero",
});
</script>

<style lang="scss" scoped>
@import "~/assets/scss/main.scss";

.section-work {
  font-size: min(5vw, 40px);
  text-align: center;
}
.section-title {
  font-size: min(5vw, 40px);
  text-align: center;
}
</style>
