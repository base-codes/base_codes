<template>
  <div>
    <nav-main />
    <Nuxt />
  </div>
</template>

<script>
import NavMain from '~/components/NavMain.vue'
export default {
  components: {
    NavMain
  }
}
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@200;400;600&display=swap");
* {
  box-sizing: border-box;
  user-select: none;
}
body {
  font-family: "IBM Plex Mono", monospace;
  background-color: #161616;
  color: #fff;
}
h1 {
  font-weight: 400;
  font-size: 96px;
  text-transform: uppercase;
}
h2 {
  font-weight: 400;
  font-size: 48px;
}
.content {
  font-weight: 200;
  font-size: 24px;
}
.sub_title {
  font-weight: 200;
  font-size: 16px;
}
hr {
  height: 1px;
  margin: 0;
}
.page-content {
  padding: 88px 160px 0;
}
</style>
