<template>
  <div class="page-content">
    <section class="intro-box">
      <div class="column is-12">
        <div class="title-box">
          <div class="sheet">
            <p>02</p>
            <p>/04</p>
          </div>
          <h1>брендинг</h1>
        </div>
        <div class="columns">
          <div class="column is-two-thirds flex">
            <div class="column el">
              <h2>Бренд-стратегия</h2>
              <p>
                Разработка и формирование платформы<br>
                бренда, тональности и стиля общения с<br>
                ЦА, миссия и ключевая метафора бренда,<br>
                позиционирование бренда
              </p>
            </div>
            <div class="column el">
              <h2>Айдентика</h2>
              <p>Разработка и формирование платформы бренда, тональности и стиля общения с ЦА, миссия и ключевая метафора бренда, позиционирование бренда</p>
            </div>
            <!-- <p>
              Разработка и продвижение веб-сайтов, веб-приложений, интернет магазинов.<br>
              Качественно прототипируем. Соблюдаем сроки. Расскажите как можно больше о своём<br>
              деле, а мы в свою очередь вникнем в ваши бизнес-процессы и создадим очень<br>
              подходящий для Вас ресурс.
            </p>
            <br>
            <p>Закажите разработку веб-сайта прямо сейчас.</p>-->
          </div>
          <div class="column links">
            <a href="#">
              перейти к работам ->
            </a>
            <a class="btn" href="#popup">
              заказать разработку
            </a>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="scss">
    .flex{
        display: flex;
    }
    .el{
        display: flex;
        flex-direction: column;
        p{
            font-size: 24px;
            font-weight: 400;
        }
    }
    .sheet{
        display: flex;
        justify-content: space-between;
        p{
          font-size: 96px;
          font-weight: 400;
        }
    }
    .links{
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      a{
        color: #fff;
      }
        .btn{
          margin-top: 25px;
          border: 2px solid #fff;
          padding: 10px 15px;
          text-align: center;
          transition: .3s ease-in;
        }
        .btn:hover{
            background: #fff;
            color: #000;
          }

      }
      .title-box{
        margin-bottom: 88px;
      }
      .intro-box{
          height: calc(100vh - 88px);
      }
</style>
