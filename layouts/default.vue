<template>
  <div class="for-scroll">
    <div class="page-noise" />
    <nav-main />
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
import NavMain from '~/components/NavMain.vue'
import Footer from '~/components/Footer.vue'
export default {
  components: {
    NavMain,
    Footer
  }
}
</script>
<style lang="scss">
$gap: 96px;

@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@200;400;600&display=swap");
@import "~bulma/bulma";

* {
  box-sizing: border-box;
  user-select: none;
  z-index: 1;
}

.page-noise {
  // background: #161616;
  width: 100%;
  height: 100%;
  position: fixed;
  left: 0;
  top: 0;
  pointer-events: none;
  z-index: 0;
  opacity: 0.4;
}
.page-noise:after {
  content: "";
  background-image: url("../assets/imgs/noise.png");
  top: -100%;
  left: -50%;
  height: 300%;
  width: 300%;
  // opacity: 0.9;
  position: fixed;
  animation: grains 8s steps(10) infinite;
}
@keyframes grains {
  0% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }

  10% {
    -webkit-transform: translate(-5%, -5%);
    transform: translate(-5%, -5%);
  }

  20% {
    -webkit-transform: translate(-10%, 5%);
    transform: translate(-10%, 5%);
  }

  30% {
    -webkit-transform: translate(5%, -10%);
    transform: translate(5%, -10%);
  }

  40% {
    -webkit-transform: translate(-5%, 15%);
    transform: translate(-5%, 15%);
  }

  50% {
    -webkit-transform: translate(-10%, 5%);
    transform: translate(-10%, 5%);
  }

  60% {
    -webkit-transform: translate(15%, 0);
    transform: translate(15%, 0);
  }

  70% {
    -webkit-transform: translate(0, 10%);
    transform: translate(0, 10%);
  }

  80% {
    -webkit-transform: translate(-15%, 0);
    transform: translate(-15%, 0);
  }

  90% {
    -webkit-transform: translate(10%, 5%);
    transform: translate(10%, 5%);
  }

  to {
    -webkit-transform: translate(5%, 0);
    transform: translate(5%, 0);
  }
}

body {
  font-family: "IBM Plex Mono", monospace;
  background-color: #161616;
  color: #fff;
  display: block;
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
h3 {
  margin-top: 10px;
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
  padding: 0px 128px;
}

@media (min-width: 1199.98px) {
  .page-content {
    padding: 0px 128px;
  }
}

.intro-box {
  height: 100vh;
  border-bottom: 1px solid #fff;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

body {
  position: relative;
}
</style>
