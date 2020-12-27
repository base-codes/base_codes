<template>
  <div>
    <div class="header">
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
.header {
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  display: flex;
  justify-content: space-between;
  padding: 32px 64px;
  background-color: #161616;
  z-index: 9999;
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
  width: 0%;
  position: absolute;
  top: 0;
  right: 0;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: flex-start;
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
    width: 90vh;
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
  position: absolute;
  overflow: hidden;
}
</style>
<script>
export default {
  data () {
    return {
      withVissible: false
    }
  },
  // закрытие меню после перехода на новую
  watch: {
    $route () {
      this.withVissible = false
      document.body.classList.remove('openedNav')
    }
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
    }
  }
}
</script>
