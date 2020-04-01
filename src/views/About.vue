<template>
  <div class="about">
    <Header/>
    <h2 class="about__ttl">PROFILE</h2>
    <div class="about__tbl">
      <div class="about__row">
        <p class="about__key">エンジニア歴</p>
        <p class="about__value">4.5年</p>
      </div>
      <div class="about__row">
        <p class="about__key">言語</p>
        <p class="about__value">HTML（Pug / EJS） / CSS （Sass / Stylus）/ JavaScript / PHP</p>
      </div>
      <div class="about__row">
        <p class="about__key">フレームワーク</p>
        <p class="about__value">Vue.js</p>
      </div>
      <div class="about__row">
        <p class="about__key">CMS</p>
        <p class="about__value">WordPress / Movable Type</p>
      </div>
      <div class="about__row">
        <p class="about__key">デザインツール</p>
        <p class="about__value">Photoshop / Sketch</p>
      </div>
      <div class="about__row">
        <p class="about__key">設計技法</p>
        <p class="about__value">アトミックデザイン / BEM / FLOCSS</p>
      </div>
      <div class="about__row">
        <p class="about__key">学習中</p>
        <p class="about__value">TypeScript / Laravel / Linux / セキュリティ</p>
      </div>
    </div>
    <ul class="about__list">
      <li class="about__item"><a href="https://github.com/am-765" target="_blank" class="about__link">GitHub</a></li>
      <li class="about__item"><a href="https://qiita.com/am_4745" target="_blank" class="about__link">Qiita</a></li>
    </ul>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'

export default {
  name: 'About',
  components: {
    Header
  }
}
</script>

<style lang="scss">

@mixin lsEm($self, $parent) {
	letter-spacing: ($self / $parent) * 1em;
}

@mixin lhCrop($lineheight) {
	&:before {
		content: '';
		display: block;
		height: 0;
		width: 0;
		margin-top: calc((1 - #{$lineheight}) * 0.5em);
	}

	&:after {
		content: '';
		display: block;
		height: 0;
		width: 0;
		margin-bottom: calc((1 - #{$lineheight}) * 0.5em);
	}
}

.about {
  height: 100vh;
  &__ttl {
    font-family: 'EB Garamond', serif;
    font-size: 20px;
    line-height: 0.75;
    text-align: center;
    padding-bottom: 40px;
  }

  &__tbl {
    max-width: 620px;
    margin: 0 auto 60px;
    border: 1px solid #999;
  }

  &__row {
    display: flex;
    flex-wrap: wrap;
    border-bottom: 1px solid #999;
    &:last-of-type {
      border-bottom: none;
    }
  }

  &__key {
    width: 129px;
    padding: 15px 0 15px 15px;
    @include lhCrop(1.5);
    border-right: 1px solid #999;
  }

  &__value {
    width: 489px;
    padding: 15px 0 15px 15px;
    font-size: 16px;
    @include lhCrop(1.5);
    padding-right: 10px;
  }

  &__list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }

  &__item {
    padding: 0 10px;
    &:not(:last-child) {
      border-right: 1px solid #333;
    }
  }

  &__link {
    position: relative;
    font-size: 16px;
    padding: 0 5px 7px;

    &::before {
      display: block;
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      transition: .3s;
      transform-origin: left;
      transform: scaleX(0);
      width: 100%;
      height: 1px;
      background-color: #333;
    }

    &:hover {
      opacity: 0.7;
      &::before {
        transition: .3s;
        transform: scaleX(1);
      }
    }
  }
}
</style>
