<template>
  <div class="career-container">
    <Tabs>
      <TabPane
        v-for="(company, index) in companies"
        :key="index"
        :label="company.name"
      >
        <div>
          <h3 class="career-title">
            <span>{{ company.job }}</span>
            <span class="company">
              <a :href="company.url" target="_blank">@{{ company.name }}</a>
            </span>
          </h3>
          <p>{{ company.during.start }} - {{ company.during.end }}</p>
          <div class="career-body">
            <ul>
              <li v-for="(content, index) in company.contents" :key="index">
                {{ content }}
              </li>
            </ul>
          </div>
        </div>
      </TabPane>
    </Tabs>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "Experience",
  data() {
    return {
      companies: [
        {
          name: "Yappli",
          job: "サーバーサイドエンジニア",
          url: "https://yappli.co.jp/",
          during: {
            start: "November 2021",
            end: "Present",
          },
          contents: ["GCP, AWSを用いた集計基盤の構築", "クーポンの機能拡張"],
        },
        {
          name: "GIBJapan",
          job: "Webエンジニア",
          url: "https://gibjapan.org/",
          during: {
            start: "January 2020",
            end: "October 2021",
          },
          contents: [
            "Laravel/Vue.jsを用いたWebアプリケーション開発",
            "メンバーの技術サポート、工数管理",
          ],
        },
        {
          name: "リアルタイムメディア",
          job: "フロントエンドエンジニア",
          url: "https://www.i-freek.co.jp/company/outline/",
          during: {
            start: "January 2019",
            end: "November 2019",
          },
          contents: [
            "Nuxt.jsを用いたフロントエンド開発",
            "Javaを用いたAndroidアプリの改修業務",
          ],
        },
      ],
    };
  },
});
</script>

<style lang="scss" scoped>
@import "~/assets/scss/main.scss";
.career-container {
  max-width: 600px;
  margin: 0 auto;
}
.section-work {
  font-size: min(5vw, 40px);
  text-align: center;
}
.section-title {
  font-size: min(5vw, 40px);
  text-align: center;
}
.career-title {
  margin-bottom: 5px;
}
.career-body {
  margin: 15px;

  li {
    margin-bottom: 3px;
  }
}
</style>

<style lang="scss">
.ivu-tabs-tab {
  color: #ccd6f6;
}
.ivu-tabs-tab-active {
  color: #64ffda !important;
  background-color: #112240;
}
.ivu-tabs-bar {
  border-bottom: 1px solid #233554;
}
.ivu-tabs-ink-bar {
  height: 3px;
  background-color: #64ffda !important;
}
</style>
