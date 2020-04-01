<template>
  <header class="header">
    <div class="header__inner">
      <h1 class="header__ttl">PORTFOLIO</h1>
      <nav class="header__nav">
        <router-link to="/works">Works</router-link> |
        <router-link to="/about">About</router-link>
      </nav>
    </div>
  </header>
</template>

<style scoped lang="scss">
.header {
  border-bottom: 1px solid #ccc;
  background-color: #fff;
  margin-bottom: 100px;
  &__inner {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    width: 1000px;
    margin: 0 auto;
    padding: 20px 0;
  }

  &__ttl {
    font-family: 'EB Garamond', serif;
    line-height: 0.75;
    font-size: 30px;
  }

  &__nav {
    font-size: 18px;
    a {
      position: relative;
      font-family: 'EB Garamond', serif;
      line-height: 0.75;
      font-size: 18px;
      padding: 0 10px 5px 10px;
      &:before {
        display: block;
        content: '';
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 1px;
        background-color: #333;
        transform: scale(0, 1);
        transform-origin: left top;
        transition: .3s;
      }
      &:hover {
        &:before {
          transform: scale(1, 1);
          transition: .3s;
        }
      }

      &.router-link-exact-active {
        color: #ccc;
        pointer-events: none;
        &:before {
          display: none;
        }
      }
    }
  }
}
</style>
