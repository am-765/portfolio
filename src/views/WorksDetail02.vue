<template>
  <div>
    <Header></Header>
    <div class="wrap">
      <div class="table">
        <div class="table__row">
          <div class="table__key">プロジェクト期間</div>
          <div class="table__val">3ヶ月</div>
        </div>
        <div class="table__row">
          <div class="table__key">プロジェクトチーム</div>
          <div class="table__val">ディレクター1名 / アートディレクター1名 / デザイナー1名 / エンジニア4名</div>
        </div>
        <div class="table__row">
          <div class="table__key">担当</div>
          <div class="table__val">設計（環境構築  / 技術選定 / コンポーネント作成 / ドキュメント作成） </div>
        </div>
        <div class="table__row">
          <div class="table__key">言語</div>
          <div class="table__val">HTML（EJS） / CSS(Sass) / JavaScript</div>
        </div>
        <div class="table__row">
          <div class="table__key">タスクランナー</div>
          <div class="table__val">gulp + webpacke</div>
        </div>
        <div class="table__row">
          <div class="table__key">バージョン管理</div>
          <div class="table__val">Git</div>
        </div>
        <div class="table__row">
          <div class="table__key">UIツール</div>
          <div class="table__val">Sketch / InVision / Zeplin</div>
        </div>
        <div class="table__row">
          <div class="table__key">サイトURL</div>
          <div class="table__val"><a href="https://www.cigr.co.jp/mp/ " target="_blank">https://www.cigr.co.jp/mp/ </a></div>
        </div>
        <div class="table__row">
          <div class="table__key">ソース</div>
          <div class="table__val"><a href="https://bitbucket.org/akihiko_machii/portfolio_05/src/master/" target="_blank">https://bitbucket.org/akihiko_machii/portfolio_05/src/master/</a></div>
        </div>
        <div class="table__row">
          <div class="table__key">進行表</div>
          <div class="table__val"><a href="https://docs.google.com/spreadsheets/d/1RenxftFltol5Olb-HpNYW8Fd1HNIxovb/edit#gid=804261452" target="_blank">https://docs.google.com/spreadsheets/d/1RenxftFltol5Olb-HpNYW8Fd1HNIxovb/edit#gid=804261452</a></div>
        </div>
        <div class="table__row">
          <div class="table__key">ポイント</div>
          <div class="table__val">
            <ul>
              <li>・ATOMICデザインによる設計</li>
              <li>・webpack導入</li>
              <li>・豊富なインタラクション</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'

export default {
  components: {
    Header
  }
}
</script>

<style lang="scss">
  .table {
    width: 100%;
    font-size: 16px;
    border: 1px solid #999;
    border-bottom: none;
    &__row {
      display: flex;
      flex-wrap: wrap;
      border-bottom: 1px solid #999;
    }
    &__key {
      width: 30%;
      padding: 15px 0 15px 15px;
      border-right: 1px solid #999;
    }

    &__val {
      width: 70%;
      padding: 15px 10px 15px 15px;
    }
  }
</style>
