<template>
  <section class="section">
    <h1 class="section-title">{{ title }}</h1>
    <slot></slot>
  </section>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "BaseSection",

  props: {
    title: {
      type: String,
      default: "",
    },
  },
});
</script>

<style lang="scss" scoped>
.section {
  margin-bottom: 12em;
}
.section-title {
  font-size: min(5vw, 40px);
  text-align: center;
  margin-bottom: 2em;
  text-transform: uppercase;
}
</style>
