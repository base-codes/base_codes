<template>
  <div>
    <div class="navbar" :class="{ 'navbar--hidden': !showNavbar }">
      <!-- из статьи -->
      <div class="logo">
        <p>
          <nuxt-link to="/">
            base
          </nuxt-link>
        </p>
      </div>
      <div class="navButton" @click="openNav">
        <span
          :class="withVissible ? 'hideMenu' : ''"
          class="btnMenu"
        >Menu</span>
        <span :class="withVissible ? '' : 'hideX'" class="btnMenu">X</span>
      </div>
    </div>

    <nav :class="withVissible ? 'fadeIn' : ''" class="">
      <div class="nav-items">
        <nuxt-link to="/">
          Главная
        </nuxt-link>
        <nuxt-link to="/web">
          Веб-разработка
        </nuxt-link>
        <nuxt-link to="/branding">
          Брендинг
        </nuxt-link>
        <nuxt-link to="/promotion">
          Продвижение
        </nuxt-link>
        <nuxt-link to="/content">
          Создание контента
        </nuxt-link>
      </div>
    </nav>
  </div>
</template>

<style lang="scss">
.navbar {
  position: fixed;
  width: 100vw;
  top: 0;
  left: 0;
  display: flex;
  justify-content: space-between;
  padding: 32px 64px;
  background-color: transparent;
  z-index: 9999;
  transform: translate3d(0, 0, 0);
  transition: 0.4s all ease-out;
}
.navbar.navbar--hidden {
  transform: translate3d(0, -100%, 0);
}
.navButton {
  color: #fff;
  cursor: pointer;
  width: 6%;
  position: relative;
  overflow: hidden;
}
.hideMenu {
  top: -110% !important;
}
.hideX {
  top: 110% !important;
}
.btnMenu {
  display: flex;
  justify-content: center;
  width: 100%;
  position: absolute;
  right: 0;
  top: 0;
  transition: 0.4s ease-in-out;
}
.logo {
  padding: 0px 15px;
  background-color: #fff;
  z-index: 10;
  a {
    color: #000;
  }
}
nav {
  width: 0;
  position: fixed;
  top: 0;
  right: 0;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  height: 100%;
  background-color: #000;
  font-size: 48px;
  font-weight: 400;
  transition: width 0.4s ease-in-out;
  overflow: hidden;
  z-index: 9998;
  .nav-items {
    display: flex;
    flex-direction: column;
    width: 90vw;
    margin-left: 64px;
    overflow: hidden;
    a {
      color: #606060;
      font-size: 64px;
      text-transform: uppercase;
    }
  }
  a:hover::before {
    content: "//";
  }
  a:hover {
    color: #fff;
  }
}
.fadeIn {
  width: 100%;
}
//отключение скрола при открытой навигации
.openedNav {
  width: 100%;
  height: 100%;
  overflow: hidden;
}
</style>
<script>
export default {
  data () {
    return {
      withVissible: false,
      showNavbar: true,
      lastScrollPosition: 0
    }
  },
  // закрытие меню после перехода на новую
  watch: {
    $route () {
      this.withVissible = false
      document.body.classList.remove('openedNav')
    }

  },
  mounted () {
    window.addEventListener('scroll', this.onScroll)
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.onScroll)
  },
  methods: {
    openNav () {
      this.withVissible = !this.withVissible
      if (this.withVissible) {
        // выключаем скролл
        document.body.classList.add('openedNav')
      } else {
        // включаем скролл
        document.body.classList.remove('openedNav')
      }
    },
    onScroll () {
      const currentScrollPosition = window.scrollY || document.documentElement.scrollTop
      if (currentScrollPosition < 0) {
        return
      }
      this.showNavbar = currentScrollPosition < this.lastScrollPosition
      this.lastScrollPosition = currentScrollPosition
    }
  }
}
</script>
