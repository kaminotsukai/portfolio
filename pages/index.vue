<template>
  <div>
    <Hero />
    <section class="about-section">
      <h1>About</h1>
      <div class="about-body">
        <div class="about-desc">
          加味真（かみまこと）と申します！私は都内のSES企業で約1年フロントエンドの開発を行う。その後、受託企業に入社し2年間で約10個のプロジェクトにWebエンジニアとして参画。ゼロイチのプロダクトが多かったため速度を追い求めつつ品質の高いサービス開発を心がける。現在は、株式会社ヤプリでノーコードプラットフォームYappliの開発にサーバーサイドエンジニアとして働いています。
        </div>
        <div>
          <img height="300" src="../static/images/profile.png" alt="profile" />
        </div>
      </div>
    </section>

    <section class="works">
      <h1>Works</h1>
    </section>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Hero from "@/components/Hero.vue";

export default Vue.extend({
  name: "IndexPage",
  components: {
    Hero,
  },
});
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Roboto+Mono:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&display=swap");
@import "~/assets/scss/main.scss";

body {
  background-color: $color-bg-theme;
  font-family: "Roboto Mono", monospace;
  padding: 0 40px;
  color: #e6f1ff;
}

.about-body {
  display: flex;
  justify-content: center;
  align-items: center;
}

@media screen and (max-width: 700px) {
  .about-body {
    flex-direction: column;
  }
}

.about-desc {
  flex: 1;
}
</style>
