<template>
  <div class="container is-fluid">
    <section class="introduction">
      <div class="columns">
        <div class="column is-12">
          <div class="columns is-gapless numbers">
            <p>04</p>
            <p>/04</p>
          </div>
          <div class="columns is-gapless">
            <h1>продвижение</h1>
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
      <div class="img-box">
        <img src="~/assets/imgs/Jpn.png">
        <div class="intro-text">
          <h1>
            выделим там<br>
            где вас обычно не замечают
          </h1>
        </div>
      </div>
    </section>
  </div>
  <!--
    <section class="cases">
      <div class="columns">
        <div class="column">
          кейсы
        </div>
        <div class="column">
          <div class="block">
            <h2>seo</h2>
            <div class="content">
              Разработка и формирование платформы бренда, тональности и стиля общения с ЦА, миссия и ключевая метафора бренда, позиционирование бренда
            </div>
          </div>
          <div class="block">
            <h2>Медиа маркетинг</h2>
            <div class="content">
              Разработка и формирование платформы бренда, тональности и стиля общения с ЦА, миссия и ключевая метафора бренда, позиционирование бренда
            </div>
          </div>
        </div>
        <div class="column">
          <div class="block">
            <h2>Контекстная реклама</h2>
            <div class="content">
              Разработка и формирование платформы бренда, тональности и стиля общения с ЦА, миссия и ключевая метафора бренда, позиционирование бренда
            </div>
          </div>
          <div class="block">
            <h2>Тагретинг</h2>
            <div class="content">
              Разработка и формирование платформы бренда, тональности и стиля общения с ЦА, миссия и ключевая метафора бренда, позиционирование бренда
            </div>
          </div>
        </div>
      </div>
    </section>
  </div> -->
</template>

<style lang="scss">
// new-verstka
.boxs{
  padding:100px 0px 200px 0px;
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
  a{
    color:#fff;
  }
  .btn {
    display: block;
    position: relative;
    margin-top: 25px;
    border: 2px solid #fff;
    padding: 10px 15px;
    text-align: center;
    transition: 0.3s ease-in-out;
    border-radius: 10rem;
    overflow: hidden;
  }
  .btn::after{
    position: absolute;
    content: "";
    top: 0;
    left: 0;
    width: 0;
    height: 100%;
    transition: all .35s;
    background: #fff;
    z-index: -1;
    border-radius: 10rem;
  }

  .btn:hover::after{
    width: 100%
  }
  .btn:hover {
    color: #000;
  }

}
    .img-box {
    position: relative;
    margin: 150px 0px 100px 0px;
    img {
      width: 100%;
    }
    .intro-text {
      position: absolute;
      top: 50%;
      right: 0;
      background-color: #161616;
    }
  }
  .cases{
      border-top: 1px solid #fff;
  }
</style>
