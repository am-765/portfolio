<template>
  <div class="works">
    <Header/>
      <div class="works__card card">
        <article class="card__card">
          <router-link to="/worksDetail01" class="card__link">
            <div class="card__imgWrap">
              <img src="../assets/imgs/img-s-groove.jpg" alt="" class="card__img" />
            </div>
            <div class="card__ttlBox">
              <h2 class="card__ttl">S-GROOVE2021新卒採用</h2>
              <p class="card__tag card__tag--renew">改修</p>
            </div>
          </router-link>
        </article>
        <article class="card__card">
          <router-link to="/worksDetail02" class="card__link">
            <div class="card__imgWrap">
              <img src="../assets/imgs/img-midpoint.jpg" alt="" class="card__img" />
            </div>
            <div class="card__ttlBox">
              <h2 class="card__ttl">MID POINT</h2>
              <p class="card__tag">リニューアル</p>
            </div>
          </router-link>
        </article>
        <article class="card__card">
          <router-link to="/worksDetail03" class="card__link">
            <div class="card__imgWrap">
              <img src="../assets/imgs/img-nakano.jpg" alt="" class="card__img" />
            </div>
            <div class="card__ttlBox">
              <h2 class="card__ttl">デュオアベニュー中野哲学堂公園</h2>
              <p class="card__tag">新規</p>
            </div>
          </router-link>
        </article>
        <article class="card__card">
          <router-link to="/worksDetail04" class="card__link">
            <div class="card__imgWrap">
              <img src="../assets/imgs/img-kinuta.jpg" alt="" class="card__img" />
            </div>
            <div class="card__ttlBox">
              <h2 class="card__ttl">プラウドシーズン世田谷砧</h2>
              <p class="card__tag">新規</p>
            </div>
          </router-link>
        </article>
        <article class="card__card">
          <router-link to="/worksDetail05" class="card__link">
            <div class="card__imgWrap">
              <img src="../assets/imgs/img-casselini.jpg" alt="" class="card__img" />
            </div>
            <div class="card__ttlBox">
              <h2 class="card__ttl">キャセリーニ LP</h2>
              <p class="card__tag">新規</p>
            </div>
          </router-link>
        </article>
        <article class="card__card">
          <router-link to="/worksDetail06" class="card__link">
            <div class="card__imgWrap">
              <img src="../assets/imgs/img-ikegami.jpg" alt="" class="card__img" />
            </div>
            <div class="card__ttlBox">
              <h2 class="card__ttl">プラウド池上</h2>
              <p class="card__tag">新規</p>
            </div>
          </router-link>
        </article>
        <article class="card__card">
          <router-link to="/worksDetail07" class="card__link">
            <div class="card__imgWrap">
              <img src="../assets/imgs/img-toho.jpg" alt="" class="card__img" />
            </div>
            <div class="card__ttlBox">
              <h2 class="card__ttl">東宝ハウス</h2>
              <p class="card__tag">リニューアル</p>
            </div>
          </router-link>
        </article>
      <!-- <p class="works__cap">※現在プロモーションが終了しているサイトにのみ、リポジトリへのリンクを掲載しています。</p> -->
      </div>
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

<style scoped lang="scss">

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

.works {
  &__card {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    width: 1000px;
    margin: 0 auto;
  }

  &__cap {
    text-align: center;
  }
}

.card {
  $this: &;


	&__card {
		position: relative;
		width: 480px;
		margin-bottom: 40px;
    border: 1px solid #ccc;
    box-shadow: 0px 1px 10px 0 rgba(0, 0, 0, 0.1);
    background-color: #fff;

		&:before {
			content: '';
			position: absolute;
			top: 0;
			left: 0;
			width: 20px;
			height: 1px;
			background-color: #333;
		}
  }

  &__img {
    transition: 1s;
  }

	&__link {
    display: block;
    height: 100%;
    padding: 20px 20px 40px;
    position: relative;

    &:after {
      content: '';
      display: block;
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 1px;
      transition: .3s;
      transform-origin: left;
      transform: scaleX(0);
      background-color: #333;
    }

    &:hover {
      &:after {
        transform: scaleX(1);
        transition: .3s;
      }

      #{$this}__img {
        transition: 1s;
        transform: scale(1.05);
      }
    }
  }

  &__imgWrap {
		position: relative;
		overflow: hidden;
  }

  &__ttlBox {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    margin: 40px 0 0;
  }

  &__ttl {
    margin-right: 20px;
    font-size: 20px;
    @include lhCrop(1.5);
  }

  &__tag {
		display: flex;
		justify-content: center;
		align-items: center;
		width: 90px;
		height: 18px;
		background-color: #02142d;
		color: #fff;
		font-size: 12px;
		line-height: 1;
		@include lsEm(2.5, 10);
		z-index: 1;
  }

  &__dataItem {
    display: flex;
    flex-wrap: wrap;
    &:not(:last-child) {
      padding-bottom: 5px;
    }
  }

  &__dataKey {
    width: 150px;
  }

  &__dataVal {
    width: calc(100% - 150px);
  }

  &__dataLink {
    position: relative;
    word-wrap: break-word;
    &::before {
      display: block;
      content: '';
      transition: .3s;
      transform-origin: right;
      transform: scaleX(1);
      width: 100%;
      height: 1px;
      position: absolute;
      bottom: 0;
      left: 0;
      background-color: #333;
    }
    &:hover {
      &::before {
        transition: .3s;
        transform: scaleX(0)
      }
    }
  }
}

@keyframes lineExtension {
	0% {
		transform: scaleX(0);
	}
	100% {
		transform: scaleX(1);
	}
}

@keyframes c {
	0% {
		transform: scaleX(1);
	}
	100% {
		transform: scaleX(0);
	}
}
</style>
