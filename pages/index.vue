<template>
  <div>
    <section class="intro">
      <div class="columns is-gapless">
        <div class="column is-12">
          <h1>Технологии и дизайн</h1>
          <div class="img-box">
            <img src="~/assets/imgs/base-gif.gif">
            <div class="intro-text">
              <p>Разработка</p>
              <p>Продвижение</p>
              <p>Поддержка</p>
            </div>
          </div>
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
  h1 {
    margin-top: 330px;
    font-size: 96px;
    font-weight: 400;
  }
  .img-box {
    position: relative;
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
}
</style>
