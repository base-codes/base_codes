<template>
  <div class="page-content">
    <section class="web">
      <div class="s">
        <div class="r">
          <p>01</p>
          <p>/04</p>
        </div>
        <h1>ВЕБ-РАЗРАБОТКА</h1>
      </div>
      <div class="s">
        <div class="columns">
          <div class="column is-two-thirds">
            <p>
              Разработка и продвижение веб-сайтов, веб-приложений, интернет магазинов.<br>
              Качественно прототипируем. Соблюдаем сроки. Расскажите как можно больше о своём<br>
              деле, а мы в свою очередь вникнем в ваши бизнес-процессы и создадим очень<br>
              подходящий для Вас ресурс.
              <br>
              Закажите разработку веб-сайта прямо сейчас.
            </p>
          </div>
          <div class="column">
            <div class="t">
              <a href="#">перейти к работам -></a>
              <a class="btn" href="#popup">
                <span>закать разработку</span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="scss">
    .r{
        display: flex;
        justify-content: space-between;
        p{
            font-size: 96px;
            font-weight: 400;
        }
    }
    .t{
        display: flex;
        flex-direction: column;
        .btn{
            padding: 10px 30px;
            text-align: center;
            border: 1px solid #fff;
            border-radius: 15px;
            display: block;
            cursor: pointer;
            color: #fff;
        }
    }

    .web{
        height: calc(100vh - 88px);
    }
</style>
