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
            <p class="list-title">内容</p>
            <ul>
              <li
                v-for="(desc, index) in company.job_descriptions"
                :key="index"
              >
                {{ desc }}
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
          name: "ヤプリ",
          job: "サーバーサイドエンジニア",
          url: "https://yappli.co.jp/",
          during: {
            start: "November 2021",
            end: "Present",
          },
          job_descriptions: [
            "Go/gRPCを用いた大規模Webアプリケーションの開発",
            "Nuxt/TypeScriptを用いたフロントエンド開発",
            "GCP, AWSを用いた集計・分析基盤の構築",
            "機能改善、インシデント対応",
          ],
        },
        {
          name: "GIBJapan",
          job: "Webエンジニア",
          url: "https://gibjapan.org/",
          during: {
            start: "January 2020",
            end: "October 2021",
          },
          job_descriptions: [
            "Laravelを用いたWebアプリケーション開発",
            "Vue.jsを用いたフロントエンド開発（主にElementUIを使用）",
            "約10個の新規サービス開発を担当",
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
          job_descriptions: [
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
  color: $color-text-main;
}
.career-body {
  margin: 15px;
  color: $color-text-main;

  li {
    margin-bottom: 3px;
  }
}
.list-title {
  margin-left: -15px;
  margin-top: 2em;
  color: $color-text-main;
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
