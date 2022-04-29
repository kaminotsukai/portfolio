<template>
  <div>
    <div class="about-body">
      <div class="about-desc">
        <p>
          加味真（かみまこと）と申します！都内のSES企業で約1年フロントエンドの開発を行った後、受託企業に入社し2年間で約10個のプロジェクトにWebエンジニアとして参画。ゼロイチのプロダクトが多かったため速度を追い求めつつ品質の高いサービス開発を心がける。現在は、株式会社ヤプリでノーコードプラットフォームYappliの開発にサーバーサイドエンジニアとして携わっています。
        </p>
      </div>
      <figure class="profile-image">
        <img src="~/assets/images/profile.png" alt="profile" />
      </figure>
    </div>
    <div class="social-icons">
      <p class="field">
        <SocialButton
          v-for="(icon, index) in icons"
          :key="index"
          :href="icon.link"
          :imageSrc="icon.imageSrc"
          :alt="icon.name"
        />
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import SocialButton from "@/components/SocialButton.vue";

export default Vue.extend({
  name: "Hero",
  components: {
    SocialButton,
  },
  data() {
    return {
      icons: [
        {
          name: "github",
          link: "https://github.com/kaminotsukai",
          imageSrc: "github-svgrepo-com.svg",
        },
        {
          name: "twitter",
          link: "https://twitter.com/kami_tsukai",
          imageSrc: "twitter-svgrepo-com.svg",
        },
        {
          name: "hatena",
          link: "https://makoo5.hatenablog.com/",
          imageSrc: "hatena-bookmark-svgrepo-com.svg",
        },
      ],
    };
  },
});
</script>

<style lang="scss" scoped>
@import "~/assets/scss/main.scss";

.about-desc {
  > p {
    font-family: "Murecho", sans-serif;
    font-weight: 300;
    line-height: 2em;
    font-size: 16px;
  }
}
.profile-image {
  > img {
    object-fit: cover;
    max-width: 240px;
    border-radius: 30px;
    margin: 40px;
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
.field {
  display: flex;
  justify-content: center;
}
</style>
