<template>
  <div class="error-wrapper">
    <section class="error-block">
      <div class="columns">
        <div class="column is-offset-3">
          <h1 v-if="error.statusCode === 404" class="headler-error">
            404
          </h1>
          <h1 v-else>
            An error occurred
          </h1>
        </div>
      </div>
    </section>
    <hr>
    <section class="erorr">
      <div class="columns columns_line">
        <div class="column is-3">
          <p>Error</p>
        </div>
        <div class="column is-6">
          <p>
            Unfortunately something went wrong. Please dubble check the URL or
            go back to the landing page. If you countinue to get this error -
            please email us at support@everydayexperiments.ikea.com
          </p>
        </div>
        <div class="column is-3">
          <div class="to-home">
            <p class="home-button" @click="toHome">
              Home page
            </p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  props: ['error'],
  methods: {
    toHome () {
      this.$router.push('/')
    }
  }
}
</script>

<style lang="scss">
.error-wrapper {
  height: 100vh;
  .error-block {
    height: 88%;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding-top: 88px;
    margin: 0 64px;
  }
  .home-button {
    padding: 16px 64px;
    border: 1px solid white;
    display: inline;
    box-sizing: border-box;
    cursor: pointer;
  }
  .to-home {
    display: flex;
    justify-content: flex-end;
  }
  .headler-error {
    font-size: 256px;
  }
}
.erorr{
    margin: 0 64px;
  }
  hr{
    margin-bottom: 24px;
  }
</style>
