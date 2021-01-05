<template>
  <div>
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
@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@200;400;600&display=swap");
* {
  box-sizing: border-box;
  user-select: none;
}
.page-noise{
  background: #161616;
  width: 100%;
  height: 100%;
  position: fixed;
  left: 0;
  top: 0;
  pointer-events: none;
  z-index: 0;
  opacity: .4;
}
.page-noise:after {
    content: "";
    background-image: url("http://api.thumbr.it/whitenoise-361x370.png?background=ffffffff&noise=9e9e9e&density=43&opacity=42");
    top: -100%;
    left: -50%;
    height: 300%;
    width: 300%;
    opacity: 0.2;
    position: fixed;
    animation: grains 8s steps(10) infinite;
}
@keyframes grains {
    0% {
        transform: translate3d(0,9rem,0)
    }

    10% {
        transform: translate3d(-1rem,-4rem,0)
    }

    20% {
        transform: translate3d(-8rem,2rem,0)
    }

    30% {
        transform: translate3d(9rem,-9rem,0)
    }

    40% {
        transform: translate3d(-2rem,7rem,0)
    }

    50% {
        transform: translate3d(-9rem,-4rem,0)
    }

    60% {
        transform: translate3d(2rem,6rem,0)
    }

    70% {
        transform: translate3d(7rem,-8rem,0)
    }

    80% {
        transform: translate3d(-9rem,1rem,0)
    }

    90% {
        transform: translate3d(6rem,-5rem,0)
    }

    to {
        transform: translate3d(-7rem,0,0)
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
// .page-content {
//   padding: 0px 128px;
// }

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

// .container.is-fluid {
//   padding-left: 160px !important;
//   padding-right: 160px !important;
// }
</style>
