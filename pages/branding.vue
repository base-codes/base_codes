<template>
  <div class="page-content">
    <section class="intro-box">
      <div class="intro">
        <div class="container is-full">
          <div class="columns">
            <div class="column is-12">
              <div class="title-box">
                <div class="sheet">
                  <p>02</p>
                  <p>/04</p>
                </div>
                <h1>брендинг</h1>
              </div>
            </div>
          </div>

          <div class="columns">
            <div class="columns">
              <div class="column">
                <h2>Бренд-стратегия</h2>
                <p>
                  Разработка и формирование платформы<br>
                  бренда, тональности и стиля общения с<br>
                  ЦА, миссия и ключевая метафора бренда,<br>
                  позиционирование бренда
                </p>
              </div>
              <div class="column">
                <h2>Айдентика</h2>
                <p>
                  Разработка и формирование платформы бренда, тональности и
                  стиля общения с ЦА, миссия и ключевая метафора бренда,
                  позиционирование бренда
                </p>
              </div>
            </div>
          </div>

          <div class="column">
            <div class="links">
              <a href="#"> перейти к работам -> </a>
              <a class="btn" href="#popup"> заказать разработку </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="about-us">
      <div class="container is-fluid">
        <div class="columns">
          <div class="column is-one-third">
            <h2>Как мы работаем</h2>
          </div>
          <div class="column">
            <p>
              Beyond can help you throughout your digital journey. We partner
              with marketing, product and board level leaders to help you
              understand your customers better - and then build the right
              products and experiences to serve them. We work with you to define
              your product vision, design a strategy and improve your business
              outcomes.
            </p>
            <div class="content">
              <h2>Нематериальные образы</h2>
              <p>
                Бренд как пропуск в особый мир, присутствие в котором иногда
                важнее самого процесса потребления.<br>
                Мы создаём ассоциации, возникающие в сознании потребителя,
                ожидания. Мы создаём ассоциации, возникающие в сознании
                потребителя, ожидания.
              </p>
            </div>
            <div class="content">
              <h2>Дизайн и проч. проч.</h2>
              <p>
                Бренд как пропуск в особый мир, присутствие в котором иногда
                важнее самого процесса потребления.<br>
                Мы создаём ассоциации, возникающие в сознании потребителя,
                ожидания. Мы создаём ассоциации, возникающие в сознании
                потребителя, ожидания.
              </p>
            </div>

            <div class="columns is-12">
              <div class="column is-half content">
                <div class="xz">
                  // хуита раз
                </div>
                <div class="xz">
                  // хуита раз
                </div>
                <div class="xz">
                  // хуита раз
                </div>
              </div>
              <div class="column content">
                <div class="xz">
                  // хуита раз
                </div>
                <div class="xz">
                  // хуита раз
                </div>
                <div class="xz">
                  // хуита раз
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="rozvoj">
      <div class="container is-fluid">
        <div class="columns description">
          <div class="column">
            подход к разработке
          </div>
        </div>
        <div class="columns">
          <div class="column is-one-third content">
            Акцентируя внимания на<br>
            типографике<br>
            и колористике мы заставляем<br>
            бренды заявлять о себе
          </div>
          <div class="column">
            <div class="photos">
              <div class="do">
                <img src="~/assets/imgs/bse.png" alt="">
              </div>
              <div class="re">
                <img src="~/assets/imgs/typo.png" alt="">
              </div>
              <div class="mi">
                <img src="~/assets/imgs/roller.png" alt="">
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="scss">
.flex {
  display: flex;
}
.el {
  display: flex;
  flex-direction: column;
  p {
    font-size: 24px;
    font-weight: 400;
  }
}

// .intro {

// }
.sheet {
  display: flex;
  justify-content: space-between;
  p {
    font-size: 96px;
    font-weight: 400;
  }
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
.title-box {
  margin-bottom: 88px;
}
.intro-box {
  height: 100vh;
  border-bottom: 1px solid #fff;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.content {
  margin: 100px 0;
  h2 {
    color: #fff;
    font-weight: 400;
  }
}
.xz {
  border-top: 1px solid #fff;
  padding: 20px 0;
}
.about-us {
  margin: 100px 0;
}
.rozvoj {
  border-top: 1px solid #fff;
}
.photos {
  display: flex;
  position: relative;
  height: 100vh;
}
</style>
