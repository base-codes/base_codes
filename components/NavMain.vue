<template>
  <div>
    <div
      class="navbars"
      :style="{ background: withVissible ? 'transparent' : '' }"
      :class="{ 'navbar--hidden': !showNavbar }"
    >
      <div v-if="!withVissible" class="page-noise" />
      <!-- из статьи -->
      <div class="logo">
        <p>
          <nuxt-link to="/">
            base
          </nuxt-link>
        </p>
      </div>
      <ul v-if="!withVissible" class="nav-items">
        <li class="item">
          <nuxt-link to="/">
            Главная
          </nuxt-link>
        </li>
        <li class="item">
          <nuxt-link to="/web">
            Веб-разработка
          </nuxt-link>
        </li>
        <li class="item">
          <nuxt-link to="/branding">
            Брендинг
          </nuxt-link>
        </li>
        <li class="item">
          <nuxt-link to="/content">
            Создание контента
          </nuxt-link>
        </li>
        <li class="item">
          <nuxt-link to="/promotion">
            Продвижение
          </nuxt-link>
        </li>
      </ul>
      <div class="navButton" @click="openNav">
        <span
          :class="withVissible ? 'hideMenu' : ''"
          class="btnMenu"
        >ЗАПОЛНИТЬ БРИФ</span>
        <span :class="withVissible ? '' : 'hideX'" class="btnMenu">X</span>
      </div>
    </div>

    <nav :class="withVissible ? 'fadeIn' : ''" class="">
      <div class="container is-fluid brief-container">
        <section class="brief">
          <h1>заполнить бриф</h1>
          <div class="columns">
            <div class="column is-3">
              <div class="control">
                <input class="input" type="text" placeholder="Как вас зовут">
                <input class="input" type="text" placeholder="E-mail">
                <input class="input" type="text" placeholder="Компания">

                <input class="input" type="text" placeholder="Должность">
                <input
                  class="input"
                  type="text"
                  placeholder="Ваш веб-сайт (при наличии)"
                >
                <input
                  class="input"
                  type="text"
                  placeholder="Планируемый бюджет"
                >
                <input
                  class="input messege"
                  type="text"
                  placeholder="Опишите задачу или прикрипите файл с описанием"
                >
              </div>
            </div>
            <div class="column is-9">
              <div class="columns sec-serv">
                <div class="column is-3 sec-serv-col">
                  <div class="column is-gapless">
                    <a
                      class="item"
                      href="#"
                      @click="toggle_web"
                    >Веб-разработка</a>
                  </div>
                  <div class="column is-gapless">
                    <a
                      class="item"
                      href="#"
                      @click="toggle_branding"
                    >Брендинг</a>
                  </div>
                  <div class="column is-gapless">
                    <a
                      class="item"
                      href="#"
                      @click="toggle_prom"
                    >Продвижение</a>
                  </div>
                  <div class="column is-gapless">
                    <a
                      class="item"
                      href="#"
                      @click="toggle_content"
                    >Создание контента</a>
                  </div>
                  <div class="column is-gapless">
                    <a class="item" href="#">Аутсорс</a>
                  </div>
                  <div class="column is-gapless">
                    <a class="item" href="#">Линчивание</a>
                  </div>
                </div>
                <div class="column is-9">
                  <div class="columns">
                    <div class="column">
                      <h3>{{ serviceitems[itemV].title_first }}</h3>
                      <div class="categ">
                        <div class="category">
                          <label for="vue">Vue</label>
                          <input id="vue" type="checkbox">
                        </div>
                        <div class="category">
                          <label for="react">React</label>
                          <input id="react" type="checkbox">
                        </div>
                        <div class="category">
                          <label for="bitrix">1C-Bitrix</label>
                          <input id="bitrix" type="checkbox">
                        </div>
                        <div class="category">
                          <label for="smthelse">Другое</label>
                          <input id="smthelse" type="checkbox">
                        </div>
                      </div>
                    </div>
                    <div class="column">
                      <h3>{{ serviceitems[itemV].title_sec }}</h3>
                      <div class="categ">
                        <div class="category">
                          <label for="tilda">Tilda</label>
                          <input id="tilda" type="checkbox">
                        </div>
                        <div class="category">
                          <label for="webflow">Webflow</label>
                          <input id="webflow" type="checkbox">
                        </div>
                      </div>
                    </div>
                    <div class="column">
                      <h3>Дополнительные услуги</h3>
                      <div class="categ">
                        <div class="category">
                          <label for="tilda">Tilda</label>
                          <input id="tilda" type="checkbox">
                        </div>
                        <div class="category">
                          <label for="webflow">Webflow</label>
                          <input id="webflow" type="checkbox">
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <p>
                Отправляя заявку, вы соглашаетесь с нашей политикой обработки
                персональных данных.
              </p>
            </div>
          </div>
          <div class="send">
            <a href="#" class="send-form"> Отправить запрос </a>
          </div>
        </section>
      </div>
    </nav>
  </div>
</template>

<style lang="scss">
.item {
  color: #fff;
  display: flex;
  justify-content: left;
}
h3 {
  margin-top: 20px;
}
.categ {
  padding-left: 15px;
  margin-top: 30px;
}
.send {
  display: flex;
  justify-content: center;
  cursor: pointer;
  .send-form {
    border: 1px solid #fff;
    padding: 10px;
    color: #fff;
    font-size: 24px;
    transition: 0.4s ease-in-out;
    &:hover {
      background: #fff;
      color: #000;
    }
  }
}
.brief-container {
  height: 100vh;
}
.brief {
  margin-top: 150px;
}
.control {
  .input {
    background: none;
    color: #fff;
    outline: 0 !important;
    box-shadow: none;
    &::placeholder {
      color: #fff;
    }
  }
}
.category {
  margin-bottom: 30px;
  &:last-child {
    margin-bottom: 0px;
  }
}
.sec-serv {
  outline: 1px solid #fff;
  outline-offset: -0.75rem;

  .sec-serv-col {
    outline: 1px solid #fff;
    outline-offset: -0.75rem;
  }
}
.nav-items {
  display: flex;
  color: #fff;
  .item {
    margin-right: 10px;
    a {
      color: #fff;
      &:hover {
        color: #606060;
      }
    }
  }
}
.item:last-child {
  margin-right: 0;
}

.navbars {
  background-color: #161616;
  position: fixed;
  width: 100vw;
  top: 0;
  left: 0;
  display: flex;
  justify-content: space-between;
  padding: 32px 96px;
  z-index: 9999;
  transform: translate3d(0, 0, 0);

  overflow: hidden;
}
.navbars.navbar--hidden {
  transform: translate3d(0, -100%, 0);
  transition: 0.4s all ease-out;
}
.navButton {
  display: block;
  color: #fff;
  cursor: pointer;
  width: 10%;
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
  font-size: 16px;
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
  height: 100vh;
  overflow: hidden;
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
</style>
<script>
export default {
  data () {
    return {
      withVissible: false,
      showNavbar: true,
      lastScrollPosition: 0,
      itemV: 0,
      serviceitems: [
        {
          title_first: 'Цифровой слэм-данк',
          title_sec: 'Быстрый старт проекта'

        },
        {
          title_first: 'Айдентификационный скачок',
          title_sec: 'Стратегический карт-бланш'
        },
        {
          title_first: 'Информационный предел',
          title_sec: 'Презентации со вкусом'
        },
        {
          title_first: 'Контекстная реклама',
          title_sec: 'SEO Bust'

        },
        {
          title_first: 'Информационный предел',
          title_sec: 'Презентации со вкусом'
        }
      ]

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
        console.log(this.showNavbar)
        console.log(currentScrollPosition)
        return
      }
      console.log(this.showNavbar + 'yes second')
      console.log(currentScrollPosition + 'second second')
      this.showNavbar = currentScrollPosition < this.lastScrollPosition
      this.lastScrollPosition = currentScrollPosition
    },
    toggleElement () {
      this.isVisible = !this.isVisible
    },
    toggle_web () {
      this.itemV = 0
    },
    toggle_branding () {
      this.itemV = 1
    },
    toggle_prom () {
      this.itemV = 2
    },
    toggle_content () {
      this.itemV = 3
    }
  }
}
</script>
