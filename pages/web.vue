<template>
  <div class="container is-fluid">
    <section class="introduction">
      <div class="columns">
        <div class="column is-12">
          <div class="columns is-gapless numbers">
            <p>01</p>
            <p>/04</p>
          </div>
          <div class="columns is-gapless">
            <h1>веб-разработка</h1>
          </div>
        </div>
      </div>
      <div class="columns">
        <div class="column is-8">
          <p>
            Разработка и продвижение веб-сайтов, веб-приложений, интернет магазинов.<br>
            Качественно прототипируем. Соблюдаем сроки. Расскажите как можно больше о своём<br>
            деле, а мы в свою очередь вникнем в ваши бизнес-процессы и создадим очень<br>
            подходящий для Вас ресурс.
          </p>
          <br>
          <p>Закажите разработку веб-сайта прямо сейчас.</p>
        </div>
        <div class="column is-4 links">
          <a href="#"> перейти к работам -> </a>
          <a class="btn" href="#popup"> заказать разработку </a>
        </div>
      </div>
    </section>

    <section class="sec-tech">
      <div class="columns">
        <div class="column is-12">
          <p class="description">
            используемые технологии
          </p>
        </div>
      </div>
      <div class="columns">
        <div class="column is-12">
          <div class="columns is-gapless">
            <div class="column">
              <div class="title">
                VUE, NUXT, WEBPACK, GULP, SCSS
              </div>
              <div class="sub_title">
                ЛЕГКО МАСШТАБИРОВАТЬ И ПОДДЕРЖИВАТЬ
              </div>
            </div>
          </div>
          <div class="columns is-gapless">
            <div class="column">
              <div class="title">
                CARBON DS, BOOTSTRAP, BULMA
              </div>
              <div class="sub_title">
                ДИЗАЙН СИСТЕМЫ, КОТОРЫЕ ПОМОГАЮТ РЕАЛИЗОВАТЬ ПРОЕКТЫ ГОРАЗДО
                БЫСТРЕЕ
              </div>
            </div>
          </div>
          <div class="columns is-gapless">
            <div class="column">
              <div class="title">
                STORYBLOK, STRAPI, PRISMIC, TILDA
              </div>
              <div class="sub_title">
                ИНТУИТИВНО ПОНЯТНЫЙ ИНТЕРФЕЙС ДЛЯ УПРАВЛЕНИЯ КОНТЕНТОМ
              </div>
            </div>
          </div>
          <div class="columns is-gapless">
            <div class="column">
              <div class="title">
                GIT
              </div>
              <div class="sub_title">
                ЧТОБЫ НИЧЕГО НЕ ЛОМАЛОСЬ
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="accordion" />
  </div>
</template>

<style lang="scss">
.introduction{
  padding: 150px 0px 100px 0px;
  border-bottom: 1px solid #fff ;

}

.numbers{
  font-size: 96px;
  display: flex;
  justify-content: space-between;
}
.links {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  a {
    color: #fff;
  }
  .btn {
    margin-top: 25px;
    border: 2px solid #fff;
    padding: 10px 15px;
    text-align: center;
    transition: 0.3s ease-in;
  }
  .btn:hover {
    background: #fff;
    color: #000;
  }
}

.intro-box {
  height: calc(100vh - 88px);
}
.title {
  font-size: 48px;
  font-weight: 400;
  color: #fff;
  margin-top: 82px;
  margin-bottom: 27px;
}
.sec-tech {
  border-bottom: 1px solid #fff;
  padding-bottom: 150px;
}
</style>
