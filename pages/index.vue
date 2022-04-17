<template>
  <div>
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

export default Vue.extend({
  name: "IndexPage",
});
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto+Mono:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&display=swap");

body {
  background-color: #0a192f;
  font-family: "Roboto Mono", monospace;
  padding: 0 40px;
  color: #e6f1ff;
}

.hero-title {
  font-size: 50px;
  color: #e6f1ff;
}
.hero-desc {
  color: #8892b0;
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
