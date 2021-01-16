<template>
  <div>
    <div class="navbars" :class="{'navbar--hidden': !showNavbar}">
      <!-- из статьи -->
      <div class="logo">
        <p>
          <nuxt-link to="/">
            base
          </nuxt-link>
        </p>
      </div>
      <ul class="nav-items">
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
          <!-- <div class="columns">
            <div class="column is-4">
              <p>компания</p>
              <p>частное лицо</p>
            </div>
            <div class="column is-8">
              услуга
            </div>
          </div> -->
          <div class="columns">
            <div class="column is-3">
              <div class="control">
                <input class="input" type="text" placeholder="Как вас зовут">
                <input class="input" type="text" placeholder="E-mail">
                <input class="input" type="text" placeholder="Компания">
                <input class="input" type="text" placeholder="Должность">
                <input class="input" type="text" placeholder="Ваш веб-сайт (при наличии)">
                <input class="input" type="text" placeholder="Планируемый бюджет">
                <input class="input messege" type="text" placeholder="Опишите задачу или прикрипите файл с описанием">
              </div>
            </div>
            <div class="column is-9">
              <div class="columns sec-serv">
                <div class="column is-3 sec-serv-col">
                  <div class="column is-gapless">
                    <label for="web">веб-разработка</label>
                    <input id="web" type="checkbox" name="">
                  </div>
                  <div class="column is-gapless">
                    <label for="branding">Брендинг</label>
                    <input id="branding" type="checkbox" name="">
                  </div>
                  <div class="column is-gapless">
                    <label for="prom">Продвижение</label>
                    <input id="prom" type="checkbox" name="">
                  </div>
                  <div class="column is-gapless">
                    <label for="content">Создание контента</label>
                    <input id="content" type="checkbox" name="">
                  </div>
                  <div class="column is-gapless">
                    <label for="outsource">Аутсорс</label>
                    <input id="outsource" type="checkbox" name="">
                  </div>
                  <div class="column is-gapless">
                    <label for="lichivanie">Линчивание</label>
                    <input id="lichivanie" type="checkbox" name="">
                  </div>
                  <a href="#">Продолжить -></a>
                </div>
                <div class="column">
                  <h3>Айдентификационный скачёк</h3>
                  <div class="categ">
                    <p class="category">
                      Vue.js
                    </p>
                    <p class="category">
                      React.js
                    </p>
                    <p class="category">
                      1C-Bitrix
                    </p>
                    <p class="category">
                      Другое...
                    </p>
                  </div>
                </div>
                <div class="column">
                  <h3>Быстрый старт-проекта</h3>
                  <div class="categ">
                    <p class="category">
                      Tilda
                    </p>
                    <p class="category">
                      Webflow
                    </p>
                  </div>
                </div>
                <div class="column">
                  <h3>Дополнительные услуги</h3>
                  <div class="categ">
                    <p class="category">
                      Tilda
                    </p>
                    <p class="category">
                      Webflow
                    </p>
                  </div>
                </div>
              </div>
              <p>
                Отправляя заявку, вы соглашаетесь с нашей
                политикой обработки персональных данных.
              </p>
            </div>
          </div>
          <div class="send">
            <a href="#" class="send-form">
              Отправить заявку
            </a>
          </div>
        </section>
      </div>
    </nav>
  </div>
</template>

<style lang="scss">
h3{
  margin-top: 10px;
}
.categ{
  padding-left: 15px;
  margin-top: 30px;
}
.send{
  display: flex;
  justify-content: center;
  cursor: pointer;
.send-form{
  border: 1px solid #fff;
  padding: 10px;
  color: #fff;
  font-size: 24px;
  transition: .4s ease-in-out;
    &:hover{
    background: #fff;
    color: #000;
  }
  }

}
.brief-container{
  height: 100vh;
}
.brief{
  margin-top: 150px;
}
.control{
  .input{
    background:none;
    color: #fff;
    outline: 0 !important;
    box-shadow: none;
  &::placeholder{
      color: #fff;
    }
  }
}
.category{
  margin-bottom: 30px;
  &:last-child{
    margin-bottom: 0px;
  }
}
.sec-serv{
  outline:1px solid #fff;
  outline-offset:-0.75rem;
  a{
    color: #fff;
    display: flex;
    justify-content: flex-end;
    padding: 20px 10px 20px 0px ;
  }
  .sec-serv-col{
    outline:1px solid #fff;
    outline-offset:-0.75rem;
  }
}
.nav-items{
  display: flex;
  color: #fff;
  .item{
    margin-right: 10px;
    a{
      color: #fff;
      &:hover{
        color: #606060;
      }
    }
  }
}
.item:last-child{
      margin-right: 0;
}

.navbars{
  position: fixed;
  width: 100vw;
  top: 0;
  left: 0;
  display: flex;
  justify-content: space-between;
  padding: 32px 16px;
  background-color: transparent;
  z-index: 9999;
  transform: translate3d(0, 0, 0);
  transition: 0.4s all ease-out;
}
.navbar.navbar--hidden {
  transform: translate3d(0, -100%, 0);
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
  height: 100vh;
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
