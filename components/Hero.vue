<template>
  <section class="hero-section">
    <div>
      <h1 class="hero-title">Makoto Kami</h1>
    </div>
    <div>
      <p class="hero-desc">Hi, I'm web developer.</p>
    </div>
    <div>
      <svg
        id="arrow-down"
        width="50px"
        height="50px"
        viewBox="0 0 24 24"
        xmlns="http://www.w3.org/2000/svg"
        color="#8892b0"
      >
        <path
          d="M15.5 7L12 10.5L8.5 7"
          stroke="currentColor"
          stroke-width="1.5"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
        <path
          d="M15.5 13L12 16.5L8.5 13"
          stroke="currentColor"
          stroke-width="1.5"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
      </svg>
    </div>
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

.hero-title {
  font-size: min(10vw, 50px);
  color: $color-text-main;
}
.hero-desc {
  font-size: min(4vw, 16px);
  color: $color-text-desc;
}
.hero-section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
.hero-section div:last-child {
  padding-top: 100px;
}
</style>
