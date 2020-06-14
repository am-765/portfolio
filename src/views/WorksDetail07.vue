<template>
  <div>
    <Header></Header>
    <div class="wrap">
      <div class="table">
        <div class="table__row">
          <div class="table__key">プロジェクト期間</div>
          <div class="table__val">2.5ヶ月</div>
        </div>
        <div class="table__row">
          <div class="table__key">プロジェクトチーム</div>
          <div class="table__val">ディレクター1名 / デザイナー1名/ エンジニア2名</div>
        </div>
        <div class="table__row">
          <div class="table__key">担当</div>
          <div class="table__val">実装 / CMS組み込み</div>
        </div>
        <div class="table__row">
          <div class="table__key">言語</div>
          <div class="table__val">HTML / CSS / JavaScript / PHP</div>
        </div>
        <div class="table__row">
          <div class="table__key">CMS</div>
          <div class="table__val">Movavel Type</div>
        </div>
        <div class="table__row">
          <div class="table__key">バージョン管理</div>
          <div class="table__val">Subversion</div>
        </div>
        <div class="table__row">
          <div class="table__key">UIツール</div>
          <div class="table__val">Photoshop</div>
        </div>
        <div class="table__row">
          <div class="table__key">サイトURL</div>
          <div class="table__val"><a href="https://thg.ne.jp/ " target="_blank">https://thg.ne.jp/</a></div>
        </div>
        <div class="table__row">
          <div class="table__key">ポイント</div>
          <div class="table__val">
            <ul>
              <li>・CMSの記事をXML出力してパース</li>
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
