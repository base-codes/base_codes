<template>
  <div>
    <Nuxt />
    <nav-main />
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
  @import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@200;400;600&display=swap');
  body{
    font-family: 'IBM Plex Mono', monospace;
  }
  h1{
    font-weight: 400;
    font-size: 96px;
  }
  h2{
    font-weight: 400;
    font-size: 48px;
  }
  .content{
    font-weight: 200;
    font-size: 24px;
  }
  .sub_title{
    font-weight: 200;
    font-size: 16px;
  }
</style>
