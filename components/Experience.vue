<template>
  <div class="career-container">
    <el-timeline>
      <el-timeline-item
        v-for="(company, index) in companies"
        :key="index"
        :timestamp="company.timestamp"
        placement="top"
      >
        <el-card>
          <h3>
            <a target="_black" :href="company.url">{{ company.name }}</a> -
            {{ company.job }}
          </h3>
          <div class="job-description">
            <ul>
              <li v-for="(job, index) in company.job_descriptions" :key="index">
                {{ job }}
              </li>
            </ul>
          </div>
        </el-card>
      </el-timeline-item>
    </el-timeline>
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
          name: "株式会社ヤプリ",
          job: "サーバーサイドエンジニア",
          url: "https://yappli.co.jp/",
          timestamp: "November 2021 - Present",
          job_descriptions: [
            "自社サービスの設計・開発・運用を担当",
            "機能改善、インシデント対応",
            "Go/gRPCを用いた大規模Webアプリケーションの開発",
            "Nuxt/TypeScriptを用いたフロントエンド開発",
            "アプリケーションのパフォーマンスチューニング",
            "GCP, AWSを用いた集計・分析基盤の構築",
          ],
        },
        {
          name: "株式会社GIBJapan",
          job: "Webエンジニア",
          url: "https://gibjapan.org/",
          timestamp: "January 2020 - October 2021",
          job_descriptions: [
            "Laravelを用いたWebアプリケーション開発",
            "Vue.jsを用いたフロントエンド開発",
            "メンバーの技術サポート、工数管理",
          ],
        },
        {
          name: "リアルタイムメディア株式会社",
          job: "フロントエンドエンジニア",
          url: "https://www.i-freek.co.jp/company/outline/",
          timestamp: "January 2019 - November 2019",
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
.job-description {
  padding: 16px;
}
.list-title {
  margin-left: -15px;
  margin-top: 2em;
  color: $color-text-main;
}
</style>

<style lang="scss">
.el-timeline-item__timestamp {
  font-size: 14px;
}
</style>
