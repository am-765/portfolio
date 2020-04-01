<template>
  <div class="top">
    <p class="top__heading">Thanks for visiting</p>
    <div class="top__nav">
      <router-link to="/works">Works</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </div>
</template>

<script>
export default {
  // name: 'HelloWorld',
  // props: {
  //   msg: String
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .top {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    width: 100vw;
    height: 100vh;

    &__heading {
      font-family: 'EB Garamond', serif;
      line-height: 0.75;
      font-size: 40px;
      padding: 30px;
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
    }
  }
}
</style>
