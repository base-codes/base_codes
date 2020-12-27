<template>
  <div>
    <section class="intro">
      <div class="columns is-gapless">
        <div class="column is-12">
          <div class="img-box">
            <h1>Технологии и дизайн</h1>
            <img src="~/assets/imgs/base-gif.gif">
            <div class="intro-text">
              <p>Разработка</p>
              <p>Продвижение</p>
              <p>Поддержка</p>
            </div>
          </div>
          <hr>
          <div class="description">
            разрабатываем, продвигаем, поддерживаем
          </div>
          <div class="columns">
            <div class="column is-two-thirds">
              <p>
                BASE.CODES УЖЕ 5 ЛЕТ НЕСЁТ<br>
                ЦИФРОВИЗАЦИЮ В МАССЫ. КОМАНДА<br>
                ЗНАЮЩАЯ РЕАЛИИ СОВРЕМЕННОГО БИЗНЕСА.<br>
                МЫ ВЗРАСТИМ НОВУЮ КУЛЬТУРУ ВАШЕЙ<br>
                ОРГАНИЗАЦИИ - КУЛЬТУРУ ТЕХНОЛОГИЙ.<br>
              </p>
            </div>
            <div class="column">
              <h1>Build<br>[Smart]</h1>
            </div>
          </div>
          <hr>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.default {
  margin: 0px 10px;
}
.intro {
  margin-top: 88px;
  padding: 0 64px;
  .img-box {
    margin-top: 330px;
    position: relative;
    margin-bottom: 96px;
    img {
      width: 100%;
    }
    .intro-text {
      position: absolute;
      bottom: 64px;
      left: 48px;
      font-size: 48px;
      background-color: #161616;
    }
  }
  .description{
    margin-top: 14px;
    font-size: 16px;
    font-weight: 400;
    color: #fff;
  }
  .column{
    color: #fff;
    margin-top: 96px;
    margin-bottom: 192px;
    p{
      line-height: 62px;
      font-size: 48px;
      font-weight: 200;
    }
    h1{
      text-align: center;
    }
  }
}
</style>
