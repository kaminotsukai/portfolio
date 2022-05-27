<template>
  <div>
    <div class="about-card">
      <div>
        <figure class="profile-image">
          <img src="~/assets/images/profile.png" alt="profile" />
        </figure>
      </div>
      <div class="about-card__right">
        <div>
          <p>Web Developer</p>
        </div>
        <div>
          <h1>Makoto Kami （{{ age }}）</h1>
        </div>
        <div>
          <p>
            加味真（かみまこと）と申します！都内のSES企業で約1年フロントエンドの開発を行った後、受託企業に入社し2年間で約10個のプロジェクトにWebエンジニアとして参画。現在は、株式会社ヤプリでノーコードプラットフォームYappliの開発にサーバーサイドエンジニアとして携わっています。
          </p>
        </div>
      </div>
    </div>
    <div class="social-icons">
      <p class="social-icons__field">
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
  computed: {
    age() {
      const today: Date = new Date();
      const birthday: Date = new Date("1999-06-18");
      return Math.floor(
        (today.getTime() - birthday.getTime()) * 3.17 * 10 ** -11
      );
    },
  },
});
</script>

<style lang="scss" scoped>
@import "~/assets/scss/main.scss";

.profile-image {
  > img {
    object-fit: cover;
    max-width: 300px;
    border-radius: 50%;
    border: 1px solid $color-text-main;
    margin: 40px;
  }
}
.about-card {
  display: flex;
  justify-content: center;
  align-items: center;

  &__right {
    flex: 1;
    > div {
      margin: 10px 0;
    }
    p {
      font-family: "Murecho", sans-serif;
      font-weight: 300;
      line-height: 25px;
    }
  }
}
@media screen and (max-width: 768px) {
  .about-card {
    flex-direction: column;
  }
}
.social-icons {
  margin-top: 10px;
  &__field {
    display: flex;
    justify-content: center;
  }
}
</style>
