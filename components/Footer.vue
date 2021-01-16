<template>
  <div class="container is-fluid">
    <h2>УСТАНОВИТЬ КОНТАКТ</h2>
    <div class="columns footerx">
      <div class="column is-8">
        <div class="columns is-gapless">
          <div class="column is-4 content">
            Социальные сети
          </div>
          <div class="column is-8">
            <a class="socials" href="#">Facebook</a>
            <a class="socials" href="#">Instagram</a>
            <a class="socials" href="#">Behance</a>
          </div>
        </div>
        <div class="columns is-gapless">
          <div class="column is-4 content">
            Контактные данные
          </div>
          <div class="column is-8">
            <a class="content" href="#">
              up@base.sss
            </a>
          </div>
        </div>
        <div class="columns is-gapless">
          <div class="column is-4 content">
            Напишите нам
          </div>
          <div class="column is-5">
            <div class="control">
              <input class="input" type="text" placeholder="Email">
              <input class="input" type="text" placeholder="Телефон">
              <input class="input messege" type="text" placeholder="Сообщение">
            </div>
          </div>
        </div>
      </div>
      <div class="column is-4">
        <div class="flex-div">
          Выбрать язык
          <select class="lang">
            <option class="option">
              Русский
            </option>
            <option class="option">
              English
            </option>
          </select>
        </div>
        <p class="copyright">
          Base all rights reserved
        </p>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.footerx{
  padding: 100px 0px;
}
.socials{
  margin-right: 20px;
  font-size: 24px;
  font-weight: 200;
  color: #fff;
  &:hover{
    color: #4d5358;
  }
}

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
  .flex-div{
    display: flex;
    flex-direction: column;
    font-size: 24px;
    font-weight: 400;
  }
  .lang{
    background: none;
    color: #fff;
    font-size: 24px;
    font-weight: 200;
    outline: none;
    border: 1px solid #555;
    cursor: pointer;
    margin-top: 20px;
    .option{
      background: #1A1A1A;
    }
  }

  .copyright{
    margin-top: 100px;
    font-size: 24px;
  }
  .input{
    margin-bottom: 20px;
    background:none;
    color: #fff;
    outline: 0 !important;
    box-shadow: none;
    &::placeholder{
      color: #fff;
    }
    &:last-child{
      margin-bottom: 0;
      height: 110px;
    }
  }

</style>>
