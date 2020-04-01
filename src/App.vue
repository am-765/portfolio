<template>
  <div id="app">
    <transition>
      <router-view/>
    </transition>
  </div>
</template>

<script>
import 'normalize.css'

export default {
  name: 'App'
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=EB+Garamond&display=swap');



#app {
  color: #333;
	font-size: 14px;
	font-family: '游明朝体', 'YuMincho', '游明朝', 'Yu Mincho', serif;
	font-feature-settings: 'palt';
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
  line-height: 1.5;
  background-color: #eee;
  padding-bottom: 100px;
}

html, body, div, span, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
abbr, address, cite, code,
del, dfn, em, img, ins, kbd, q, samp,
small, strong, sub, sup, var,
b, i,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, figcaption, figure,
footer, header, hgroup, menu, nav, section, summary,
time, mark, audio, video {
    margin: 0;
    padding: 0;
    border: 0;
    outline: 0;
    font-size: 100%;
    vertical-align: baseline;
    background: transparent;
}

article, aside, details, figcaption, figure,
footer, header, hgroup, menu, nav, section {
    display: block;
}

body {
    line-height: 1;
}

ol, ul {
    list-style: none;
}

blockquote, q {
    quotes: none;
}

blockquote:before, blockquote:after,
q:before, q:after {
    content: '';
    content: none;
}

a {
    margin: 0;
    padding: 0;
    font-size: 100%;
    vertical-align: baseline;
    background: transparent;
}

img {
    vertical-align: bottom;
}

table {
    border-collapse: collapse;
    border-spacing: 0;
}

del, ins {
    text-decoration: none;
}

caption, th {
	text-align: left;
}

h1, h2, h3, h4, h5, h6 {
	font-size: 1em;
	font-weight: normal;
}

mark {
    font-style: italic;
    font-weight: bold;
}

abbr, acronym {
  border: 0;
  font-variant: normal;
}

sup {
  font-size: 0.75em;
  vertical-align: 0.25em;
}

sub {
  font-size: 0.75em;
  vertical-align: -0.25em;
}

big {
  font-size: 110%;
}

small {
  font-size: 90%;
}

legend {
  color: #000000;
}

hr {
  display: block;
  height: 1px;
  border: 0;
  border-top: 1px solid #cccccc;
  margin: 1em 0;
  padding: 0;
}

input, button, textarea, select, optgroup, option {
	font-family: inherit;
	font-size: inherit;
	font-style: inherit;
	font-weight: inherit;
  vertical-align: middle;
}

body {
  // color: #333;
	// font-size: 14px;
	// font-family: '游明朝体', 'YuMincho', '游明朝', 'Yu Mincho', serif;
	// font-feature-settings: 'palt';
	// -webkit-font-smoothing: antialiased;
	// -moz-osx-font-smoothing: grayscale;
}

*,
*:before,
*:after {
	box-sizing: border-box;
}

img {
	max-width: 100%;
	height: auto;
	vertical-align: top;
}

a {
  color: #333;
	text-decoration: none;
}

.wrap {
  width: 1000px;
  margin: 0 auto;
}


.header {
  border-bottom: 1px solid #ccc;
  &__inner {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    width: 1000px;
    margin: 0 auto;
    padding: 20px 0;
  }

  &__ttl {
    font-family: 'EB Garamond', serif;
    line-height: 0.75;
    font-size: 40px;
  }
}

.v-enter {
  transform: translate(-100px, 0);
  opacity: 0;
}
.v-enter-to {
  opacity: 1;
}
.v-enter-active {
  transition: all 1s 0s ease;
}
.v-leave {
  transform: translate(0, 0);
  opacity: 1;
}
.v-leave-to {
  transform: translate(100px, 0);
  opacity: 0;
}
.v-leave-active {
  transition: all .5s 0s ease;
}

</style>
