<template>
  <a class="social-btn" :href="link" target="_blank">
    <img :src="require(`@/assets/images/${imageSrc}`)" :alt="alt" />
  </a>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "SocialButton",
  props: {
    imageSrc: {
      type: String,
      default: "",
      required: true,
    },
    alt: {
      type: String,
      default: "",
      required: true,
    },
    link: {
      type: String,
      default: "",
      required: true,
    },
  },
});
</script>

<style lang="scss" scoped>
@import "~/assets/scss/main.scss";

.social-btn {
  height: 47px;
  width: 47px;
  border: 1px solid $color-text-main;
  border-radius: 100%;
  margin: 0 10px;
  display: flex;
  justify-content: center;
  align-items: center;

  > img {
    height: 20px;
    width: 20px;
  }
}
</style>
