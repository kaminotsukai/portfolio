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
            <p class="list-title">業務内容</p>
            <ul>
              <li
                v-for="(desc, index) in company.job_descriptions"
                :key="index"
              >
                {{ desc }}
              </li>
            </ul>

            <p class="list-title">経験</p>
            <ul>
              <li
                v-for="(experience, index) in company.experiences"
                :key="index"
              >
                {{ experience }}
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
            "Yappliの設計・開発",
            "機能改善、インシデント対応",
          ],
          experiences: [
            "Go/gRPCを用いたWebアプリケーションの開発",
            "Nuxt/TypeScriptを用いたフロントエンド開発",
            "GCP, AWSを用いた集計・分析基盤の構築",
            "testingパッケージを用いた単体テストの作成",
            "AppsFlyer Data Lockerを利用したBigQueryへのローデータエクスポート",
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
            "Laravel/Vue.jsを用いたWebアプリケーション開発",
            "メンバーの技術サポート、工数管理",
          ],
          experiences: [
            "不動産売買システムの新規開発",
            "不動産ポータルサイトの新規開発",
            "学習支援サービスの開発",
            "チャットボット管理システムの開発",
            "M&Aマッチングサービスのプロトタイプ開発",
            "サプリメントECサイトのリプレース業務",
            "Pupeteerを用いたスクレイピングスクリプトの作成",
            "Stripeを用いた決済処理の作成",
            "Line Messaging SDKを用いたチャットボットの開発",
            "Slackへのアラート通知作成",
            "AWSを用いたインフラの構築",
            "PHPUnitによる単体テストの導入",
            "AdobeXDを用いたデザインカンプの作成",
            "Pub, Stylusを用いたLPの作成",
            "issue駆動開発の導入",
            "コーディング規約の策定",
            "Dockerによるローカル開発の導入",
            "クライアント用のドキュメント作成",
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
          experiences: [
            "オンラインストレージサービスのリプレース業務",
            "チャットアプリの改修業務",
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
