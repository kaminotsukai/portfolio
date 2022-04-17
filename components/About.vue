<template>
  <section class="about-section">
    <h1 class="section-title">About...</h1>
    <div class="about-body">
      <div class="about-desc">
        <p>
          加味真（かみまこと）と申します！都内のSES企業で約1年フロントエンドの開発を行った後、受託企業に入社し2年間で約10個のプロジェクトにWebエンジニアとして参画。ゼロイチのプロダクトが多かったため速度を追い求めつつ品質の高いサービス開発を心がける。現在は、株式会社ヤプリでノーコードプラットフォームYappliの開発にサーバーサイドエンジニアとして携わっています。
        </p>
      </div>
      <figure class="profile-image">
        <img src="/images/profile.png" alt="profile" />
      </figure>
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

.about-section {
  height: 100vh;
}
.section-title {
  font-size: min(5vw, 40px);
  text-align: center;
}
.about-desc {
  > p {
    font-family: "Murecho", sans-serif;
    font-weight: 200;
    line-height: 2em;
  }
}
.profile-image {
  > img {
    object-fit: cover;
    max-width: 240px;
    border-radius: 30px;
  }
}
.about-body {
  display: flex;
  justify-content: center;
  align-items: center;
}
@media screen and (max-width: 768px) {
  .about-body {
    flex-direction: column;
  }
}

.about-desc {
  flex: 1;
}
</style>
