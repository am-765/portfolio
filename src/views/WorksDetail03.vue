<template>
  <div>
    <Header></Header>
    <div class="wrap">
      <div class="table">
        <div class="table__row">
          <div class="table__key">プロジェクト期間</div>
          <div class="table__val">1.5ヶ月</div>
        </div>
        <div class="table__row">
          <div class="table__key">プロジェクトチーム</div>
          <div class="table__val">ディレクター1名 / アートディレクター1名 / デザイナー1名 / エンジニア2名</div>
        </div>
        <div class="table__row">
          <div class="table__key">担当</div>
          <div class="table__val">実装</div>
        </div>
        <div class="table__row">
          <div class="table__key">言語</div>
          <div class="table__val">HTML（EJS） / CSS(Sass) / JavaScript</div>
        </div>
        <div class="table__row">
          <div class="table__key">タスクランナー</div>
          <div class="table__val">Prepros（GUIコンパイラ）</div>
        </div>
        <div class="table__row">
          <div class="table__key">バージョン管理</div>
          <div class="table__val">Git</div>
        </div>
        <div class="table__row">
          <div class="table__key">UIツール</div>
          <div class="table__val">Photoshop / Zeplin</div>
        </div>
        <div class="table__row">
          <div class="table__key">サイトURL</div>
          <div class="table__val"><a href="https://zjhghjnlzbghh-portfolio-03.herokuapp.com/dev/index.html" target="_blank">https://zjhghjnlzbghh-portfolio-03.herokuapp.com/dev/index.html </a></div>
        </div>
        <div class="table__row">
          <div class="table__key">ポイント</div>
          <div class="table__val">
            <ul>
              <li>・テキストエフェクト</li>
              <li>・ホバーエフェクト</li>
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
