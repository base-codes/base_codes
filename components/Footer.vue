<template>
  <div class="container is-fluid">
    <div class="columns">
      <div class="column is-2">
        <p class="content">
          Социальные сети
        </p>
        <p class="content">
          Контактные данные
        </p>
        <p class="content">
          Напишите нам
        </p>
      </div>
      <div class="column is-6">
        <div class="socials">
          <a class="content" href="#">Facebook</a>
          <a class="content" href="#">Instagram</a>
          <a class="content" href="#">Behance</a>
        </div>
        <p class="contact">
          8-(800)-888-88-88
        </p>
        <p class="contact">
          up@base.sss
        </p>
        <div class="field">
          <input class="input is-success" type="text" placeholder="Text input" value="">
        </div>
      </div>
      <div class="column is-4">
        <p class="content">
          Выбрать язык
        </p>
        <a class="btn" href="#">Русский</a>
        <p class="content">
          Base all rights is reserved
        </p>
      </div>
    </div>
  </div>
</template>
<style scoped>

  .contact{
    font-size: 24px;
    font-weight: 200;
  }
  .content{
    color: #fff;
  }
  .content:last-child{
    margin-top: 100px;
  }
  .socials{
    margin-bottom: 30px;
  }
</style>
